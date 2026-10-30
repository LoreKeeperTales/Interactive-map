Ellond 451 token folder

The default token is default_campaign (circled in your screenshot).
Make sure its actual file extension is .png. If it is .jpg, .webp, or .svg, change the filename in tokens/token-list.js AND the fallback in index.html accordingly. Windows Explorer hides extensions by default.

Place all token images in this folder. This patch does NOT include your artwork; keep your existing images.

The selector reads filenames from token-list.js. Edit that list to match your actual filenames and extensions (including capitalization).

Campaign JSON stores only tokens/<filename>, never image bytes. Replacing the image at the same path automatically changes its appearance for every saved campaign when reloaded (browser cache may need refreshing).

The token images remain in your repository; they are not copied into JSON saves.
