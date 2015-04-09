# Ragnarson HTML and CSS Style Guide

* Follow the rules from [Mark Otto's Code Guide][code-guide]

* Use [autoprefixer][autoprefixer] or [autoprefixer-rails][autoprefixer-rails]

* Use the following naming convention:

  ```html
    <!-- Objects -->
    <div class="media"></div>
    <a class="btn"></a>

    <!-- Object with a related sub-object -->
    <div class="media">
      <img class="media-img"></div>
      <div class="media-body"></div>
    </div>

    <!-- Object with modifier -->
    <div class="media media-milli"></div>
    <a class="btn btn-primary"></a>

    <!-- Object with state -->
    <a class="btn is-btn-active"></a>
    <a class="btn is-btn-disabled"></a>

    <!-- Object which requires wrapper -->
    <!-- f.e. "position: relative" and "position: absolute" pair -->
    <div class="box has-close-link">
      <a class="close-link"></a>
    </div>

    <!-- JavaScript handler -->
    <div class="alert js-alert"></div>
  ```

* Avoid styling generic HTML elements:

  ```css
    /* bad */
    p {
      ...
    }

    /* good */
    .blog-post-body > p {
      ...
    }
  ```

* Avoid nested classes:

  ```css
    /* bad */
    .blog-post .meta .author {
      ...
    }

    /* good */
    .blog-post-meta-author {
      ...
    }
  ```

* Never use the HTML id attribute in stylesheets:

  ```css
    /* bad */
    #headline {
      ...
    }

    /* good */
    .headline {
      ...
    }
  ```

[code-guide]: http://codeguide.co/#css
[autoprefixer]: https://github.com/postcss/autoprefixer
[autoprefixer-rails]: https://github.com/ai/autoprefixer-rails
