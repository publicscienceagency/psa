# Public Science Agency (PSA)

this is our site (WIP)

- `/theme` is where you change the layout and styling of the site
- `/content` is where you change the content and data that is rendered in the site

---

## setup

the site runs on [`port`](https://github.com/frnsys/port), so install that first.

then clone this repo and `cd` into it.

then link up the directories and config to their proper places:

    ln -sf $PWD/content ~/.port/psa
    ln -sf $PWD/theme ~/.port/themes/psa
    ln -sf $PWD/conf.yaml ~/.port/psa.yaml

then build the initial site:

    port build psa

cool, now you can boot up a `port` server:

    port serve psa

it'll be viewable at `localhost:5005`.

then whenever you change stuff in the `content` dir, rebuild before you refresh:

    port build psa

---

if you change the theme sass, be sure to recompile it:

    sass theme/css/main.sass theme/css/main.css

---

## a note on setting up the embedded HOSNY replayer

    git submodule update --init --recursive
    cd theme/hosny
    npm install -d
    npm run build

then you can `port build psa` etc

if you make changes to HOSNY replay, then update here with the following:

    cd theme/hosny
    git pull
    npm run build
    port build psa