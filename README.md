# Steam Banners: Data

## Store banners

This folder contains Steam store **banners** downloaded with the tool provided in my [`download-steam-banners`](https://github.com/woctezuma/download-steam-banners) repository (also available as [a Google Colab notebook][download_steam_banners]).
[![Open In Colab][colab-badge]][download_steam_banners]

### Small horizontal banners (460x215)

-   original images (460x215 resolution, with a few exceptions) in [`data/`](data/),
-   resized images (128x128 resolution) in [`banners/128x128.zip`](https://drive.google.com/open?id=1YLhdwgnhyP-eC4gHOmTsmuiUSr0XN5XJ).

### Large horizontal banners (616x353)

As of February 2020, additional Steam banners are provided on Google Drive:
-   original horizontal images (natively 616x353 resolution) in [`original_horizontal_steam_banners.tar`](https://drive.google.com/open?id=1-0FrkH3X1Eji6bDbGNYRTo9_C4PIfqlb).

### Vertical banners (300x450)

As of February 2020, additional Steam banners are provided on Google Drive:
-   original vertical images (300x450 resolution, introduced [after the Steam libary update in October 2019](https://steamcommunity.com/games/593110/announcements/detail/1666821776739358716), currently available for 42% of games) in [`original_vertical_steam_banners.tar`](https://drive.google.com/open?id=1KZ4_eiB4TTZqIwTJOQYzgDvbVXXhEqOe),
-   resized vertical images (128x128 resolution) in [`vertical_steam_banners/128x128.zip`](https://drive.google.com/open?id=1_H3ejjM45yteTbECCk1FJ3KJNjB1995b),
-   resized vertical images (256x256 resolution) in [`vertical_steam_banners/256x256.zip`](https://drive.google.com/open?id=1_H3ejjM45yteTbECCk1FJ3KJNjB1995b).

As of August 2020:
-   original vertical images (300x450 resolution, currently available for 19049 out of 37813 games, i.e. 50% of games) in [`original_vertical_steam_banners.tar`](https://drive.google.com/file/d/1_a5GfVZYKD4oz-ctTyjSwu_pAhoBNwEm/view?usp=sharing),
-   resized vertical images (256x256 resolution) in [`resized_vertical_steam_banners.tar`](https://drive.google.com/file/d/1-4IrxRMetTjCDQI60oMg4hs7NIcMy286/view?usp=sharing).

### Logos (640x360)

As of September 2020, a selection of logo images is shared [on Google Drive][logos-google-drive]:
-   original logo images (640x360 resolution, PNG files) in [`original_steam_logos_640x360.tar.gz`][logos-original],
-   resized logo images (256x256 resolution, PNG files) in [`resized_steam_logos_256x256.tar.gz`][logos-resized].

Initially, there are 25851 logos out of 45421 games, i.e. 57% of games.
My selection of logo images include 21279 logos, i.e. 82% of logos, after removal of:
-   4117 logos with uncommon resolution (anything but 640x360),
-   455 blank or duplicate logos.

**Caveat**: be careful if you use logos, as they are PNG files and feature [a transparent background][transparent-images].

## Screenshots

Steam **screenshots** can be found in [`download-steam-screenshots-data`](https://github.com/woctezuma/download-steam-screenshots-data):
-   original images (inconsistent resolution, at most 600x338),
-   center-cropped and resized images (128x128 resolution).

<!-- Definitions -->

[download_steam_banners]: <https://colab.research.google.com/github/woctezuma/google-colab/blob/master/download_steam_banners.ipynb>

[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>

[logos-google-drive]: <https://drive.google.com/drive/folders/1_xVdBziq3uIRx53x_s28G7TvTcM5skA1?usp=sharing>
[logos-original]: <https://drive.google.com/file/d/1wNGQyx2rL-mPmPcF8LbbvbFmqH9Zl5RT/view?usp=sharing>
[logos-resized]: <https://drive.google.com/file/d/1wNfO2zYvn3u4DnobnE4JJDiQ_Of_Vwsb/view?usp=sharing>
[transparent-images]: <https://github.com/lucidrains/stylegan2-pytorch#bonus>
