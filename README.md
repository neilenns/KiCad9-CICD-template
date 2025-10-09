# KiCad 9 CI/CD Template

This template is meant to be used with cookiecutter and GitHub, not cloned directly. To use:

## Run the cookiecutter script to generate a new project

```powershell
pip install cookiecutter
cookiecutter https://github.com/neilenns/KiCad9-CICD-template
```

Then follow the prompts.

## Create a new GitHub repository

Use GitHub to make a new, empty repository.

After generating the project with cookiecutter, push the new project to your GitHub repository:

```bash
cd <your-project-directory>
git init
git remote add origin <your-repo-url>
git add .
git commit -m "Initial commit"
git push -u origin main
```

## Grant GitHub Actions access to your repository

In the GitHub UI, go to Settings > Actions > General and enable both **Read and write permissions** and **Allow GitHub Actions to create and approve pull requests** under **Workflow permissions**.
