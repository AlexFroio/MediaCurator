# MediaCurator

MediaCurator is a Python command line tool to manage a media database. 
* List all the video’s and their information with or without filters
* Batch find and repair/convert videos with encoding errors
* Batch recode videos to more modern codecs (x265 / AV1) based on filters: extentions, codecs, resolutions …

## Documentation

The documentation is available on the following [link](https://fabquenneville.github.io/MediaCurator/)

## Usage
./curator.py [list,convert] [-del] [-in:any,avi,mkv,wmv,mpg,mp4,m4v,flv,vid] [-filters:fferror,old,lowres,hd,720p,1080p,uhd,mpeg,mpeg4,x264,wmv3,wmv] [-out:mkv/mp4,x265/av1]  [-print:list,formated,verbose] [-dir/-files:"/mnt/media/",,"/mnt/media2/"]

> for multiple files or filenames use double comma separated values ",,"

default options are:
-in:any
-filters:
-out:mkv,x265
-print:list

Examples:
```bash
./curator.py list -filters:old -print:formated -dir:/mnt/media/ >> ../medlist.txt
./curator.py convert -del -filters:mpeg4 -out:av1,mp4 -dir:"/mnt/media/Movies/"
./curator.py convert -del -in:avi,mpg -print:formated,verbose -dir:/mnt/media/
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[GNU GPLv3](https://choosealicense.com/licenses/gpl-3.0/)