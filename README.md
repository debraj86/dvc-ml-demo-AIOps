"dvc-ml-demo-AIOps" \
move to the folder \2_26th_sep_2021\
echo "# dvc-ml-demo-AIOps" >> README.md
git init
git add README.md
git config --global user.email debraj86ghosh@gmail.com
git config --global user.name debraj86
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/debraj86/dvc-ml-demo-AIOps.git
git push -u origin main
dvc init
mkdir -p src\utils
create dvc.yaml, config.yaml etc
Inorder to install all local packages including src packag, inside requirements.txt at the end write the following command
-e . 
then perform 
pip install -r requirements.txt # for instaiing the local package src
then run the following command
python src\stage_01_load_save.py
run with a specific parameter
python src\stage_01_load_save.py --config=params.yaml
run with option -c 
python src\stage_01_load_save.py -c param.yaml
next run
python src\stage_01_load_save.py
then create the pipeline stages in dvc.yaml
run 
dvc repro

ERROR: failed to reproduce 'dvc.yaml':  output 'artifacts\raw_local_dir\data.csv' is already tracked by SCM (e.g. Git).
    You can remove it from Git, then add to DVC.
        To stop tracking from Git:
            git rm -r --cached 'artifacts\raw_local_dir\data.csv'
            git commit -m "stop tracking artifacts\raw_local_dir\data.csv"
In order to get rid of this error perform the command
git rm -r --cached "artifacts/raw_local_dir/data.csv"
git commit -m "stop tracking artifacts\raw_local_dir\data.csv"


