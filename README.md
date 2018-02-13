# GitHub Pages + Jekyll Tests

This page contains tests I've done with Jekyll via Github Pages. I will give you the results of theses tests below.


## Make Jekyll works with GitHub Pages

I've done an simple Jekyll setup using the [guide in the official website](https://jekyllrb.com/) and configured the website by editing the [_config.yml file](./docs/_config.yml).

To make Jekyll compatible with GitHub Pages, I've commented `gem "jekyll"` line and uncommented `gem "github-pages"` in Gemfile, after, I've executed the `bundle install` command.

I've got an error from Bundler:

Some gems are not compatible with the `github-pages` gem.
```
Bundler could not find compatible versions for gem "jekyll-feed":
  In snapshot (Gemfile.lock):
    jekyll-feed (= 0.9.3)

  In Gemfile:
    github-pages was resolved to 36, which depends on
      jekyll-feed (= 0.2.3)

    minima (~> 2.0) was resolved to 2.3.0, which depends on
      jekyll-feed (~> 0.9)

Running `bundle update` will rebuild your snapshot from scratch, using only
the gems in your Gemfile, which may resolve the conflict.

Bundler could not find compatible versions for gem "liquid":
  In snapshot (Gemfile.lock):
    liquid (= 4.0.0)

  In Gemfile:
    github-pages was resolved to 6, which depends on
      liquid (= 2.5.2)

    minima (~> 2.0) was resolved to 2.3.0, which depends on
      jekyll (~> 3.5) was resolved to 3.7.2, which depends on
        liquid (~> 4.0)

Running `bundle update` will rebuild your snapshot from scratch, using only
the gems in your Gemfile, which may resolve the conflict.

Bundler could not find compatible versions for gem "minima":
  In snapshot (Gemfile.lock):
    minima (= 2.3.0)

  In Gemfile:
    minima (~> 2.0)

    github-pages was resolved to 94, which depends on
      minima (= 1.0.1)

Running `bundle update` will rebuild your snapshot from scratch, using only
the gems in your Gemfile, which may resolve the conflict.
```
Okay, it says to do the `bundle update` command, so I've done it to see if it fixes the problem.

After the execution of the `bundle update` command, I've retried to do `bundle install`.

It worked! Now I'll push to GitHub to see if Jekyll works with GitHub Pages now.

The website seems to work pretty well, now I'll try to write a new post.

## Write a blog post
Now, we have a functionnal website made with Jekyll.
So, let's write an article on it!

I created a markdown file in the [_posts](./docs/_posts/) folder with the name format `YYYY-MM-DD-name-of-post.markdown` and I copied the welcome post and changed it.

So, now we have our first blog post!