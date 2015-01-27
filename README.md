# static-gallery
so. gallery3 gets discontinued...

A set of jinja2 templates and modified RST syntax. that creates a static html gallery from folders of pictures.

For each folder there might be a _configure.py file which configures things like access rights, template to render, inheritance of these atrributes.

Their might also be a album.rst containing a album description. and a imagename.ext.rst which contains image specific text. I might even write a editor for these rst files in the future 

Uploading will be done by creating a temporary system user with the intended target dir as home directory. then you can ssh/rsync/scp what has you.

Auth will be done by basic http auth for this the script will generate appropriate .htacess files and nginx configurations.

There shall be a way to only partially render for new folders.

Imagemagick will be used for resizing (I like the content aware scaling, sorry...)

Also there will be a default Template it will have square content awarely scaled previews and a lightbox style image enlarge function.

Javascript will be kept to a minimum

except for the upload page there will be no dynamic content. 

each folder will contain a file, containing its own name encrypted with a key only the server knows, the upload page will only accept such keys as input. gallery creation can only be done by a mighty wizzard.

