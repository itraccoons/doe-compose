# doe-compose

###### _repo-stub for now_

#### Example:

    $ mkdir -p ~/workspace/try
    $ cd ~/workspace/try
    $ cat > doe-compose.yml
    ---
    pip:
      install: --user
        - yamllint
    builtin:
      export:
        - PATH=~/.local/bin:$PATH
      eval:
        - yamllint --strict ./doe-compose.yml; [ $? -ne 0 ] && exit

    doe:
      modules:
        - pull
      install:
        - appengine-java-sdk 1.9.60
      nomulus:
        - pull
        - build
    ...
    $ doe compose up

#### More

Look into

https://github.com/itraccoons/doe-modules (compose, modules, nomulus)

and

https://github.com/itraccoons/nomulusx

