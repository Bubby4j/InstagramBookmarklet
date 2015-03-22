# InstagramBookmarklet
A bookmarklet for downloading photos off the Instagram website (PC only)

# Usage
Run the bookmarklet and then CTRL + CLICK any image on someone's instagram profile to download it at full resolution.

# Bookmarklet
Drag this to your bookmarks bar
<a href="javascript:var imgs=$('.pgmiImageLink');for(i=0;i<imgs.length;i++){var url=imgs.find('.iImage')[i].style.backgroundImage.replace("url(","").replace(")","");$(imgs[i]).attr('href',url);$(imgs[i]).attr('download',i+'.jpg');}">InstagramDownload</a>

# Source
    var imgs = $('.pgmiImageLink');
    for(i = 0; i < imgs.length; i++)
    {
        var url = imgs.find('.iImage')[i].style.backgroundImage.replace("url(", "").replace(")","");
        $(imgs[i]).attr('href', url);
        $(imgs[i]).attr('download', i + '.jpg');
    }
  
