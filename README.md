# LiteraryAI 
[![Gem Version](https://badge.fury.io/rb/wax_theme.svg)](https://badge.fury.io/rb/wax_tasks)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![CI:Test](https://github.com/minicomp/wax/workflows/ci:test/badge.svg)](https://github.com/minicomp/wax/actions?query=workflow%3Aci%3Atest)
[![Depfu](https://badges.depfu.com/badges/9d4da973f2cd2680c11ca34738c2dfb2/overview.svg)](https://depfu.com/github/minicomp/wax?project_id=10550)
[![Gem Downloads](https://img.shields.io/gem/dt/wax_theme.svg?color=046d0b)](https://badge.fury.io/rb/wax_theme)
[![Join the chat the minicomp-wax channel of the Code4Lib Slack](https://img.shields.io/badge/Slack-%23minicomp--wax-brightgreen.svg)](https://docs.google.com/forms/d/e/1FAIpQLSeD77mBp0Y13mFePF8UmDwFrlbxNx3VttEjz_3dgglJeK-Zbg/viewform?c=0&w=1)
![License](https://img.shields.io/github/license/minicomp/wax_tasks.svg?color=c6a1e0)

#### The Literary History of Artificial Intelligence is a collaboration between the Columbia English Department, the Columbia University Rare Books & Manuscript Library, and Columbia University’s Digital Scholarship department. The digital exhibit explores the long, shared history of literature and computation through the Columbia Library’s holdings.
  
## Basic Information:

- __Contact:__ Jeremiah Mercurio, Digital Scholarship
- __Target url:__ https://literaryai.library.columbia.edu/
- __Target host type:__ s3
- __Bucket:__ cul-s3-dlst-travis-litai-prod
  
## Features:

- [ ] __Active updates?__ 
- [ ] __Relational data?__
- [ ] __Student contributions?__
- [ ] __Custom search?__
- [ ] __IIIF?__ 
- [ ] __Maps?__
- [ ] __D3?__
- [ ] __Other:__ None

## Dependencies

### JS (i.e. runtime)
- Jquery 3.2.1

### Ruby (i.e. dev/test)
- Jekyll 4.1
- Kramdown parser

## Branches

#### `main`: The up-to-date production branch (Jekyll/back-end). 
- Travis pushed compiled site to `static` branch after tests passed.
- Using s3, Travis deploys compiled site to s3 prod bucket after tests pass.

#### `staging` : The staging branch (Jekyll/back-end)
- Created only as a copy

#### `static` : The up-to-date compiled production site (static HTML)
- Built and pushed by Travis on successful commit to `main` branch.



## Contributing (non-admin)

[Not taking new contributions, but just in case]

1. Clone the repository: `$ git clone https://github.com/REPO-NAME`
2. Install dependencies: `$ cd REPO-NAME && bundle`
3. Checkout your own branch: `$ git checkout -b MY-FEATURE`
4. Make your changes
5. Run tests locally: `$ bundle exec rake wax:test`
6. Push branch to remote repository.
7. Sumbit a PR to merge your branch into staging.
8. If tests pass, confirm merge into `staging` and delete your branch. This will trigger a deployment of the compiled site from staging to the `gh-pages` branch (and if you're using s3, to the staging bucket).
9. Preview the staged site (either at cul.github.io/REPO-NAME or the staging s3 bucket). If it looks good, submit a PR to merge staging into master.
10. If the tests from the PR pass, an admin will accept the merge, and Travis will deploy a backup/copy of the compiled site to the `static` branch (and if you're using s3, it will deploy to the prod s3 bucket as well).


## Travis deployment set-up

https://wiki.library.columbia.edu/pages/viewpage.action?spaceKey=USGSERVICES&title=Set+up+static+site+deployment+to+s3
