# {{ cookiecutter.project_name}}

This generated project is ready for use with KiCad 9. It includes the necessary GitHub workflows to create output files for JLCPCB fabrication when a release is created in GitHub. The project is intended to be used with the amazing [JLCPCB KiCad library](https://github.com/jlcpcb/KiCad-Libraries).

It also includes a devcontainer to enable local production of the output files using the same environment as the GitHub workflows. To create the output, run the following command:

```bash
mkdir -p release/JLCPCB
kicad-cli jobset run --file jobs.kicad_jobset "{{ cookiecutter.project_name }}.kicad_pro"
```

Note that the output will not include the post-processing steps done by the GitHub workflow to prepare the BOM and POS files for JLCPCB.

After a release the repo will be updated with top and bottom board images in the `docs/` folder. These can be inserted into the `README.md` if desired.
