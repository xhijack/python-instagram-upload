# python-instagram-upload #

Upload and post photos to [Instagram](http://instagram.com) with Python!

This is inspired and roughly ported from the PHP implementation by
[Lance Newman](http://lancenewman.me/posting-a-photo-to-instagram-without-a-phone/).

And this refactor (from https://github.com/lukecyca/python-instagram-upload)

Usage Example:

    filepath = "/tmp/square.jpg"
    insta = InstagramSession(USERNAME, PASSWORD)
    if insta.login(USERNAME, PASSWORD):
        insta.upload_photo(filepath, "hello Instagram")
        
Note that photos must be square to be uploaded. You can convert your
photo using ImageMagick with this command:

    convert -define jpeg:size=1280x1280 -resize 640x640^ \
        -extent 640x640 /tmp/original.jpg /tmp/square.jpg
