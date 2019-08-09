CM = colmap
TYPE = COLMAP

all:
	date +"%c" > TIMEIT
	$(CM) feature_extractor --database_path ./database.db --image_path ./images
	$(CM) exhaustive_matcher --database_path ./database.db
	mkdir sparse
	$(CM) mapper --database_path ./database.db --image_path ./images --output_path ./sparse
	mkdir dense
	$(CM) image_undistorter --image_path ./images/ --input_path ./sparse/0 --output_path ./dense --output_type $(TYPE) --max_image_size 2000
	$(CM) patch_match_stereo --workspace_path ./dense/ --workspace_format $(TYPE) --PatchMatchStereo.geom_consistency true
	$(CM) stereo_fusion  --workspace_path ./dense/ --workspace_format COLMAP --input_type geometric --output_path ./dense/fused.ply
	date +"%c" >> TIMEIT
