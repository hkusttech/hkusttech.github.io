## hkusttech

The static website for HKUST Tech Club, generated by [Hugo](https://gohugo.io/)

### Hugo Setup


- [Install Hugo](https://gohugo.io/getting-started/installing/)
- Hugo is a static website generator. It should be installed globally.

```sh
git clone https://github.com/hkusttech/hkusttech.github.io.git
cd hkusttech.github.io        # change to the project directory
yarn                          # install dependencies
```

### GitHub page 

- `master` branch is used for the deployed website. It is required by **GitHub** for an organization page
- `dev` branch is used for hosting the source codes. 

```sh
git checkout dev             # Switch to the dev branch
git branch                   # Verify that you are in dev
git pull                     # receive the latest update
```

### How to publish a new event?

- Simple. No need to modify **ANY HTML**
- Inside the `content/events` folder
  - Copy `template` folder *(or create a new folder)* as `[new event name]`
    - Put images (*.png, *.jpg, ...) and other content for this event
  - Copy `template.md` and rename it as a `[new event name].md`
    - Change from `draft: true` to `draft: false`
    - Change the date 
    - Modify the tags 
    - Edit the content using **markdown** language. [Markdown reference](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### How to test the website?

```sh
yarn run debug    # Debug, all draft content will be included
yarn run build    # Build the web site content in the public folder (only non-draft content will be included) 
```

### How to deploy?

```sh
yarn run deploy   # Deploy to the github page. 
```