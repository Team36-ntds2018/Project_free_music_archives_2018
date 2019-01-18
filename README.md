# NTDS project: Transitional playlists for new musical discoveries

This project is done in the frame of the EPFL course *Network tour of data science*.
The main goal is to take some of the most listened tracks found in the *Free Music Archive* and help someone wishing to discover a new style or a new artist to transition smoothly from a song he knows and likes to an other unknown music. Basically the idea is to let the user choose two points in a graph representing the music tracks and return him a 10(max)-tracks playlist gradually changing from musics similar to the first track to others more like the the second track.

## Code and notebooks

- `Load_save_dataset.ipynb` loads the metadata from the dataset used in this project. The data with scripts to process it can be found [on the fma github repository](https://github.com/mdeff/fma), it is contained in this archive: [fma_metadata.zip](https://os.unil.cloud.switch.ch/fma/fma_metadata.zip). The two files used for this project are `tracks.csv` and `echonest.csv`, the relative path to these files can be modified at the beginning of the notebook. 
This first notebook loads the data with the Pandas library, keeps a subset to create and save an adjacency matrix as well as key features of the selected music tracks.

- `Project_ntds_2018_team36.ipynb` loads and uses the data processed by the first notebook. Previously generated files can be found in the `Project generated files` folder. It uses the NetworkX library to create a graph out of the adjacency matrix and compute paths between selected nodes (music tracks) to create a new playlist.
It is important to NOT run the whole notebook in one go! The user should click on the two desired nodes in the graph created in section **Node selection** before running subsequent cells.


## Dependencies:
- numpy
- pandas
- matplotlib
- scipy
- math
- collections
- pyunlocbox
- networkx
