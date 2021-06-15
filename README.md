An Augmented Reality project by Pragya Madaan 
- using PiFuHD to generate 3D models from low-resolution 2D images (with different background, lighting and views)
- visualizing depth maps for 2D images and the generated 3D models,
- generating 3D avatar in Blender for one of the selected 3D models 
- placing the avatar in real world through Instagram filters using SparkAR


--------------------------------------------------------------------------------------------------------------------------------

This file contains the instructions for running the code in the following parts:

I) DEPTH MAP GENERATION
- Step1: Upload the CodeLibrary_2DtoDepth on your Google Drive [preferably at the path /content/drive/My Drive/TCD Sem2/Augmented Reality/Project DepthMap/2dtodepth/ , else you need to change the path in .ipynb file]
- Step2: All the inputs are to be uploaded in the folder named "infile" and all the outputs will be generated in the folder named "outfile". The inputs and outputs of "Stylize-me project" from these folders have been cleared from these folders, as instructed. However, for multiple runs of the code on your end, you might wish to clean the inputs before ecah run.
- Step3: Open GoogleColab and upload "DepthMapGeneration.ipynb" file there.
- Step4: Change the Colab Runtime Type to 'GPU' and mount your Google Drive to Colab by running the first cell. Once authenticated, run the next cells (referring step 1&2) and check the output depth maps in "outfile" once done.

II) 2D IMAGE TO 3D MESH & ITS VIDEO GENERATION USING PiFuHD
- Step1: Create the folders required on your Google Drive for the path of "CodeLibrary_PiFuHD" [preferably at the path /content/drive/My Drive/TCD Sem2/Augmented Reality/Project/ , else you need to change the path being referred in the .ipynb file] 
- Step2: Open GoogleColab and upload "PiFuHD Mesh Generation.ipynb" file there. Provide Google Authentication to it and enable GPU runtime. Then, run the initial cells which are outlining to clone PiFuHD github repositories. Once they're downloaded, they will be stored in your Google Drive and you donot have to clone it on your next code run.
- Step3: All the inputs are to be uploaded in the folder named "sample_images" which lies under "pifuhd" folder. For multiple runs of the code on your end, you might need to remove all of the generated files from your previous run and add the 2D image(s) you wish to test with. 
- Step4: In case of multiple runs, it is recommended to clear all the data from output images folder whose path is "results/pifuhd_final/recon/" within the "pifuhd" folder before the start of any new experiment on this code base. This will ensure that nothing gets overwritten and fresh results are produced.
- Step5: After adding the input 2D images, start running all the next cells one by one. Now, check the files containing output meshes (.obj and .png) files at "results/pifuhd_final/recon/" in your Google Drive folder once all the cells have been run. You may also have a look at the generated .txt files for the input 2D images by checking the "sample_images" folder.
- Step6: After the outputs have been generated, Open GoogleColab and upload "PiFuHD Video Generation.ipynb" file there. This is to produce short video consisting of each input 2D image and its 3D mesh. 
- Step7: Authenticate google drive, check colab runtime and also check the image filenames mentioned in the "files" list. Change them to match with your image input filenames, if required. 
- Step8: Run the cells in Colab notebook and once all of it is finished, you will notice the .mp4 files generated in the "results/pifuhd_final/recon/" within the "pifuhd" folder. 

While Stylize-me has used its generated .obj files within Blender for Avatar creation, the generated .mp4 files or .obj files at your end can be further utilised for various other purposes.


 
--------------------------------------------------------------------------------------------------------------------------------
Please Note: The previously added input 2D images for "Stylize-me project", their generated .txt files and their respective outputs are already cleaned from the folder. Moreover, I have added commands in PiFuHD mesh generation .ipynb notebook to clone PiFuHD and pose estimation repository at your end. In case of any queries, please feel free to reach out.
