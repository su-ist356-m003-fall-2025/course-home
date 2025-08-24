# SU-OSPO Workshop Template

## Purpose

The aim of this template is to provide a set structure for the organisation of content and materials for workshops run by [Syracuse University OSPO](https://opensource.syracuse.edu). It is established for the internal SU-OSPO team and is therefore specific to our needs. However, if useful, anyone is free to download or reuse the template for their own purposes.

## Instructions

So, we're doing another workshop are we!? Follow this helpful checklist to get started with this template.

1. On the main page of the repository, click 'Use this template' (top right) and select 'Create a new repository'.
2. Enter a suitable repository name for the workshop, including the topic, season, and/or year.
3. You are now ready to start creating your workshop content and materials. Start by updating the `README.md` file in the repository. You may wish to include information about the workshop (e.g., who it is run by, where and when, funding support, etc) and archiving information ([see below](#archiving)).
4. At this point you should edit the `index.qmd` in the top-level of the directory. There is placeholder text in the file, so just update accordingly!
5. You can now prepare your course materials. Each unit of the workshop should have a designated folder (with an informative name). Placeholder folders have been included (e.g., `01_UNIT_NAME`), which you can rename, delete, or add to as you please. Within each unit folder, you should have an `index.qmd` file. This is the landing file you should populate for the given unit. As with the root `index.qmd` file, the `title` in this file will be used in the navigation menu.
6. **In order to ensure that the units are listed in the desired order in the navigation menu, the `order` attribute in the YAML of each `index.qmd` file should be updated to reflect the desired order of the units (e.g., the `index.qmd` file in the first unit should have `order: 1`, the `index.qmd` file in the second unit should have `order: 2`, etc).**
7. (optional) Within each unit folder, you can also have other .qmd files if you need to organize your content across multiple pages. You should again use the `order` attribute to determine the order of these pages in the navigation menu. You are welcome to also include other materials in these unit folders, including, but not limited to, images, scripts, and data files. You can structure your materials as you please, but in general, we recommend being organised - this means having a dedicated folder structure such as `materials/data`. **When linking between pages, linking to other materials, or including images, make sure to use relative paths instead of absolute paths.** You may also use full URLs if linking to external materials or including external images.

## Archiving

We strongly recommend that you archive your workshop materials. Archiving should be done via continuous integration with Zenodo, implemented through version controlled releases (a manual process when all content has been prepared). You can follow the [instructions here](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content) to link your GitHub repository to Zenodo and set up automatic archiving whenever a new release is created.

## Folder structure and content

```bash
workshop-template
├── README.md
├── index.qmd
├── 01_UNIT_NAME
│   └── index.qmd
├── 02_UNIT_NAME
│   └── index.qmd
├── 03_UNIT_NAME
│   └── index.qmd
├── images
│   └── logo.png
├── LICENSE
├── workshop.Rproj
├── .github
│   └── workflows
│       └── publish.yml
└── .gitignore
```