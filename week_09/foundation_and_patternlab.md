# Integrate Foundation Into Pattern Lab


Git clone Pattern Lab

`git clone git@github.com:pattern-lab/patternlab-php.git`

`cd patternlab-php`

Make sure Pattern Lab has been generated with 

`php core/builder.php -g`

Inside of Pattern Lab, in the *source* folder, start a new Foundation project using Compass:

`foundation new foundation`

Remove any *.git* folders within the newly create *source/foundation* folder.

Copy *source/foundation/scss/_settings.scss* to *source/css/scss/_settings.scss*

Create a *config.rb* file at *source/css/config.rb* with at least the following:

	# Require any additional compass plugins here.
	add_import_path "../foundation/bower_components/foundation/scss"
	add_import_path "../foundation/scss"

	# Set this to the root of your project when deployed:
	http_path = "/"
	css_dir = "/"
	sass_dir = "/"

Finally, in *source/css/style.scss* include the following lines to use Foundation:

	@import "scss/settings";
	@import "foundation";

You can now edit *source/css/scss/_settings.scss* to make all the variable changes needed to customize Foundation. You can write your Sass and Sass partials like normal withing *source/css/style.scss*.

Compile your .scss files using `compass watch` or `compass compile` within *source/css*.

