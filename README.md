# InstagramBookmarklet
A bookmarklet for downloading photos off the Instagram website (PC only)

## Usage
Run the bookmarklet and then CTRL + CLICK any image on someone's instagram profile to download it at full resolution.

# Bookmarklet
Add this to your bookmark bar
```javascript
javascript:var imgs=$('.pgmiImageLink');for(i=0;i<imgs.length;i++){var url=imgs.find('.iImage')[i].style.backgroundImage.replace("url(","").replace(")","");$(imgs[i]).attr('href',url);$(imgs[i]).attr('download',i+'.jpg');}
```

#### Source
```javascript
var imgs = $('.pgmiImageLink');
for(i = 0; i < imgs.length; i++)
{
    var url = imgs.find('.iImage')[i].style.backgroundImage.replace("url(", "").replace(")","");
    $(imgs[i]).attr('href', url);
    $(imgs[i]).attr('download', i + '.jpg');
}
```
