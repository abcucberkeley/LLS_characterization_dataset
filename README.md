# LLS_characterization_dataset

The dataset is uploading to a public data repository now. The link and the DOI will be provided here once the uploading is done. 

The image data is organized for the figures in the paper Characterization, Comparison, and Optimization of Lattice Light Sheets (https://doi.org/10.1101/2022.07.30.502108):

Within a figure folder:
*    **xzPSF.tif**: xz PSF of the light sheet for the figure
*    **cellData**: folder contains the experimental data
    
Within **cellData**:
 *   **Data**: image data for cultured cells with ER labeling
 *   **PSF**: experimental PSFs for 20ms and 2ms exposure time
    
Within ./cellData/Data:
*    **20ms**: cell data with 20ms exposure
*   **2ms_ts**: time series image data with 2ms exposure
    
Within **./cellData/Data/20ms**:
*    **tif, csv, json, txt, sqlite3** files are the cell image data and meta data with 20ms exposure
*    **DSR**: deskew/rotated data for raw cell image data; MIPs within DSR folder contains the max intensity projection image for 3D deskew/rotated stacks.
*    **gaussian_weighted**: data with 1d smoothed enveloped weights with gaussian smoothing (the intermediate images are not included).
    
Within **./cellData/Data/20ms/gaussian_weighted**:
*    **matlab_decon**: RL deconvolution results for data weighted with 1d smoothed envelope.
    
Within **./cellData/Data/20ms/gaussian_weighted/matlab_decon**:
*    **1_debug** or **3_debug**: saving deconvolution results every 5 iterations till 200 iterations
*    **psfgen**: preprocessed PSF (removing background; remove empty regions) as input for the deconvolution program
    
Within **./cellData/Data/20ms/gaussian_weighted/matlab_decon/1_debug (or 3_debug)**:
*    tif files are deconvolution results saved every 5 interations (in skewed space)
*    **DSR**: deskew/rotated data for deconvolution results in the folder; MIPs within DSR folder contains the max intensity projection image for 3D deskew/rotated stacks.

Within **./cellData/Data/2ms_ts**:
*    tif, csv, json, txt, sqlite3 files are the cell image data and meta data with 2ms exposure; there are 100 time points.
*    **gaussian_weighted**: data with 1d smoothed enveloped weights with gaussian smoothing (the intermediate images are not included).
    
Within **./cellData/Data/2ms_ts/gaussian_weighted/matlab_decon**:
*    tif files are deconvolution results for given iterations (optimal number of iterations determined with Fourier Shell Correlation), in skewed space.
*    **MIPs**: the max intensity projection images for the tiff files in the folder.
*    **DSR**: deskew/rotated data for deconvolution results in the folder; MIPs within DSR folder contains the max intensity projection image for 3D deskew/rotated stacks.
