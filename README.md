"dvc-ml-demo-AIOps" 
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

