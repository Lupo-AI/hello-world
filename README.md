# Hello World Template

We provide this template with the minimum requirements for lupo to generate your custom videos.

Please feel free to modify it and adapt it to your needs. 

If you need help, do not hesitate to contact us. We will be more than happy to help our customers and adapt our product to your needs.

## What is included:

```
hello-world
├── .github
│   └── workflows
│       └── generate-course.yml
├── .vscode
│   ├── customsnippets.code-snippets
│   ├── extensions.json
│   └── settings.json
├── sample
│   └── sample.md
├── themes
│   └── customtheme.md
├── README.md
└── toc.yml
```

* `.github/workflows/generate-course.yml`: contains the github action to generate the videos based on the content of this repository.
* `.vscode/customsnippets.code-snippets`: contains snippets or shorcuts to save you time when creating the same slides multiple times. More about snippets in Advanced > Snippets.
* `.vscode/extensions.json`: contains suggested extensions that will pop up if you don't have them installed when you open your project for the first time. 
* `.vscode/settings.json`: contains suggested configurations for VSCode or its extensions. Here is where we add the themes. More about themes and customization in Styling.
* `sample/sample.md`: the content that will be generated is inside this file. The name and location of it could be anything, because the order, names and location of each markdown file is specified inside the toc.yml.
* `README.md`: its a regular github readme file. It is totally optional.
* `toc.yml`: its the most important file in order to generate your videos. Contains all the information and configuration required by lupo. 