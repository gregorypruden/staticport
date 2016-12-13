# staticport
## A static portfolio framework 

The idea is to take a bunch of folders with photos in them and build a static website to run on Amazon S3 or other static hosting platform.
Maybe it should be called jBof.  It should organize the folders into categories and allow routes/URLs to go directly to that category's page.

'staticport OPTIONS [path]`

### OPTIONS could be:
`-theme <sometheme>`
`-ignorenonimages`
`-rootfolder`
`-contactformurl`

Maybe it assumes the images are in an images folder in [path] and uses that as the root unless -rootfolder is provided.  Otherwise assumes folders in path are the categories in the resulting page.

[path]
  |
  images
      wildlife
        birds
        butterflies
      fashion
      Events
        Event1
      Fine Art
        Project1
        Project2

if it finds a file with the same name except txt or json or html it will use that caption the image.  This behavior would be negated by using the -ignorenonimages switch.

It should have a default theme that is applied.  That theme should be very nice with lots of options.  

The -contactformurl would point to an api or lambda function to send the contact email or signup for a email list.

