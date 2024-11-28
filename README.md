# ODT_pipeline
The pipeline consists of 7 steps:
#1) Hologram aquisition
#2) Field retrieval
#3) Tomogram reconstruction
#4) cell Mask aqusition
#5) Field retrieval with YOLOv8 cellMap
#6) Tomogram reconstruction (again)
#7) Cell quantification
   
![data_analysis_pipelines](https://github.com/user-attachments/assets/bd74de51-2289-4ebd-8d06-9e402b308788)

The updated data analysis pipeline: after hologram acquisition (#1), field retrieval (#2), and tomogram reconstruction (#3), the YOLOv8 model is applied to the MIP of reconstructed tomograms to retrieve cell masks (#4). Upon acquisition, the cell map was applied to a field retrieval step once again (#5), which allowed us to distinguish the background from cell cytoplasm better. The obtained phase maps were further used in the tomogram reconstruction algorithm (#6). In the last step of the data analysis, the cell map was used again (#7). The resulting pipeline showed better performance and better estimated quantification.
