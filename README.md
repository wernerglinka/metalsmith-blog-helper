# metalsmith-blog-helper

## Blog Helper Lists
This Metalsmith plugin helps to show blog info like:

* All Blogs
* Recent Blogs
* Featured Blogs
* Annualized Blogs List

### All Blogs

This list provides the sorted array **allSortedBlogPosts** that provides the following info for each blog post:

* Title
* Date
* Author
* Path
* Image

This list can be essential if the blog implementation uses paging and a block showing all other blog posts by a particular author are needed.

### Recent Blogs

This plugin provides the array **latestBlogPosts**. The number of listed blog posts is determined by option **latest_quantity**

### Featured Blogs

This plugin provides the array **featuredBlogPosts**. Blog posts can specify in their Front Matter if the post should be listed and what position it should have in the list. Blog posts intended to be listed should have set:

_featured_blog_post: true_

_featured_blog_post_order:_ <integer>

The plugin will use two additional option values:

_featured_blog_post_sort_order: "asc" | "desc"_

_featured_quantity:_ <integer>

### Annualized Blogs List

This plugin provides the associative array **annualizedBlogPosts**. All blog posts are listed by their creation year.

## Install



## Usage

````
var blogLists = require('metalsmith-blog-helper');
.
.
.
.use(blogLists({
  "latest_quantity": 4,                       // length of the recent posts list
  "featured_quantity": 2,                     // length of the featured posts list
  "featured_blog_post_sort_order": "desc"
}))
````