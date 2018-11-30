# Deployment and Development Instructions


## update repo
These commands are a little redundant, but do them all & you should be fine:

``` shell
git clone --recursive git@github.com:khangchendzonga/khangchendzonga.github.io.git
cd khangchendzonga.github.io
git submodule sync
git submodule update --init --recursive
```

## Change Content

add pages to `content/page/`. Follow yaml examplesi n headers of existing pages.

## Experiment with themes

You can easily fool around with supported themes by pointing hugo at the theme-specific config file when you run the server locally. So for instance, to use the `hugo-now-ui` theme run this command: 

``` shell
# first `cd` to root directory of the site
hugo server  -w  --config now-config.toml -p 39444 --navigateToChanged 

```
then open `localhost:39444` in your browser.

## change themes

``` shell
cp THEME-SPECIFIC-config.toml config.toml
# commit changes in atom or whatever
# push change sin atom or whatever
```
Site will update automatically.  
