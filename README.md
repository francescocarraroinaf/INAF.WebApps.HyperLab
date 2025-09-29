# INAF.WebApps.HyperLab

## License
This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0).  
[Learn more](https://creativecommons.org/licenses/by-nc/4.0/)

The project hosted on GitHub represents only the main component and does not include all the libraries required to build and run the full solution. All related projects that make up the complete solution are maintained on GitLab. To retrieve the full solution, please use the script provided below. This process requires creating a GitLab account and generating a Personal Access Token with the read_repository permission.

# ---------------------------------------- #
#!/bin/bash
#set main projects folder
projects_folder_path="[your_project_path]"
pat_name="[pat_name]"
pat_value="[pat_value]"

cd $projects_folder_path

mkdir $projects_folder_path/INAF
mkdir $projects_folder_path/INAF/Libraries
mkdir $projects_folder_path/INAF/Libraries/Net
mkdir $projects_folder_path/INAF/Libraries/Net/HyperLab
mkdir $projects_folder_path/INAF/Libraries/Net/DB


git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/DotNET/WebApps/INAF.WebApps.HyperLab.git $projects_folder_path/INAF/WebApps/INAF.WebApps.HyperLab

cd $projects_folder_path/INAF/Libraries/Net
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/CommonWebApps/INAF.Libraries.Net.CommonWebAppHelpers.git
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/CommonWebApps/INAF.Libraries.Net.CommonWebAppModels.git

git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/INAF.Libraries.Net.Extensions.git
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/INAF.Libraries.Net.Log.git
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/INAF.Libraries.Net.Math.git
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/INAF.Libraries.Net.Parallelization.git
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/INAF.Libraries.Net.ScienceModels.git

git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/DotNET/Libraries/Net/DB/INAF.Libraries.Net.DB.HyperLab.Data.git $projects_folder_path/INAF/Libraries/Net/DB/INAF.Libraries.Net.DB.HyperLab.Data
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/DotNET/Libraries/Net/DB/INAF.Libraries.DB.Net.HyperLab.Users.git $projects_folder_path/INAF/Libraries/Net/DB/INAF.Libraries.Net.DB.HyperLab.Users

git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/HyperLab/INAF.Libraries.Net.HyperLab.CommonHelpers.git $projects_folder_path/INAF/Libraries/Net/HyperLab/INAF.Libraries.Net.HyperLab.CommonHelpers
git clone https://$pat_name:$pat_value@www.ict.inaf.it/gitlab/francesco-carraro/Libraries/Net/HyperLab/INAF.Libraries.Net.HyperLab.CommonModels.git $projects_folder_path/INAF/Libraries/Net/HyperLab/INAF.Libraries.Net.HyperLab.CommonModels
# ---------------------------------------- #

Full functionality of the web app also depends on connecting to its corresponding database, which is not provided in this repository. You will need to configure and supply the appropriate database instance separately to enable complete operation.

For any help or question, write to francesco.carraro at inaf.it
