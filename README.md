# test03

TL;DR Project test03 was committed on 6/18/2021 with no README.md. It was a successful project as it has achieved
* First experience with Jekyll, a static blog platform (much simpler than Ruby on Rails) written in Ruby
* Local interaction between a local server (bundle exec jekyll serve) and a local browser (http://localhost:4000/)
* Remote interaction between a remote server (https://kuolai.github.io/test03/) with any browser
* Deploy to github.io (Github Pages) with gh-pages branch and git push command (It is tricky to a noobie)

Problems arised as I revisited test03 project three months later and I did not know
* What test03 project tried to do
* Why I did not write a README
* What have I learned from it
* Why there are so many untracked files in working dir? Shall I abandoned them or committed them?
* What shall I put into README so I (hopefully others too) will not get lost again

Now I know what a README can do (kudos to [Tania Rascia](taniarascia.com)) and here is the README three months late
* It has a link to demo its functionality
* It has a tutorial link to trace all steps you did/learned with comments
* It tells where your local repo is

Tutorial (TBD)/[See demo here](https://kuolai.github.io/test03/)
----

Tutorial [git local out of date]
* Scenario: 
* Remote: README.md is created; but Local: does not know the change
* Local: $git status #show nothing changed, however $git remote show origin shows local out of date
* A bit more complicated in this case of gh-pages branch at both sides

$ git remote show origin
* remote origin
  Fetch URL: https://github.com/kuolai/test03.git
  Push  URL: https://github.com/kuolai/test03.git
  HEAD branch: main
  Remote branches:
    gh-pages tracked
    main     tracked
  Local ref configured for 'git push':
    gh-pages pushes to gh-pages (local out of date)

$ git branch --set-upstream-to=origin/gh-pages gh-pages
Branch 'gh-pages' set up to track remote branch 'gh-pages' from 'origin'.

$ git remote show origin
* remote origin
  Fetch URL: https://github.com/kuolai/test03.git
  Push  URL: https://github.com/kuolai/test03.git
  HEAD branch: main
  Remote branches:
    gh-pages tracked
    main     tracked
  Local branch configured for 'git pull':
    gh-pages merges with remote gh-pages
  Local ref configured for 'git push':
    gh-pages pushes to gh-pages (local out of date)

$ git pull
Updating 8082140..46b5e44
Fast-forward
 README.md | 25 +++++++++++++++++++++++++
 1 file changed, 25 insertions(+)
 create mode 100644 README.md


Tags: jekyll, github pages, git deployment
