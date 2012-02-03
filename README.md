# Acts As Commentable

Allows for comments to be added to multiple and different models.

### Forked
* Added Rails 3.2 support
* Removed default scope on comments

### Installation

`gem install "acts_as_commentable"`

 If using bundler then just add 
`gem "acts_as_commentable"` to your Gemfile 
and
`bundle install`

Generate your comment model:

`rails g comment`

Then migrate your database:

`rake db:migrate`

### Usage
 
 Make your ActiveRecord model act as commentable.

	class Post < ActiveRecord::Base
		acts_as_commentable
	end

 Add a comment to a model instance

	post = Post.create
	post.comments.create(:comment => "my first comment!")

 Fetch comments for a commentable model:

	post = Post.find(1)
	comments = post.comments.recent.limit(10).all


### Credits

**Xelipe** - This plugin is heavily influenced by Acts As Taggable.

###### Contributors

Jack Dempsey, Chris Eppstein, Jim Ray, Matthew Van Horn, Ole Riesenberg, ZhangJinzhu, maddox, monocle

###### More

[http://www.juixe.com/techknow/index.php/2006/06/18/acts-as-commentable-plugin/](http://www.juixe.com/techknow/index.php/2006/06/18/acts-as-commentable-plugin/)
[http://www.juixe.com/projects/acts_as_commentable](http://www.juixe.com/projects/acts_as_commentable)
