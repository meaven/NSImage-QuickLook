# NSImage+QuickLook

`NSImage+QuickLook` by [Matt Gemmell](http://mattgemmell.com/source/) provides Finder-like preview icons for files.

This is a category on NSImage which lets you get an image containing a Quick Look preview of the content of a given file. If no Quick Look preview is available, it will instead return the file's Finder icon (this is what the Quick Look panel does). It consists of only one method:

    + (NSImage *)imageWithPreviewOfFileAtPath:(NSString *)path ofSize:(NSSize)size asIcon:(BOOL)asIcon

Path should be a full file-system path (i.e. you should do `-stringByExpandingTildeInPath` etc before passing the path to this method).

Size is an `NSSize` giving the maximum size of the preview image, obviously.

The last parameter is a `BOOL` indicating whether the preview should be rendered as an icon, i.e. with a document border, drop-shadow, page-curl and file-type/extension superimposed. Pass `YES` to get Finder-style icon previews, or pass `NO` to get previews like those in the Quick Look panel.


## Usage

Simply copy the two files into your project, and make sure your active target imports the QuickLook framework.


## License

Please see the Source Code License document accompanying the source.
