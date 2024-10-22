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

As of October 2020, I have filtered Steam banners ([provided on Google Drive][banners-google-drive]) to ensure higher data quality:
-   original vertical images (300x450 resolution, available for 16933 out of 46032 games, i.e. 37% of games) in [`original_vertical_steam_banners.tar`][banners-original],
-   filtered vertical images (300x450 resolution, available for a subset of 14176 games) in [`filtered_vertical_steam_banners.tar`][banners-filtered],
-   resized vertical images (256x256 resolution, 14176 games) in [`resized_vertical_steam_banners.tar`][banners-resized],
-   resized vertical images (256x256 resolution, 14000 games after a second filtering) in [`resized_vertical_steam_banners_14k.tar`][banners-resized-14k].

Filtering of banner images consists in the removal of:
-   banners with uncommon bands (anything but RGB),
-   banners with less than 100% image space used by content (to avoid learning [vignetting][vignetting-wiki]),
-   duplicate banners,
-   outliers with respect to file size (to try to have banners of similar visual complexity).

There was no case of:
-   banners with uncommon resolution (anything but 300x450),
-   blank banners.

Filtering of duplicates, outliers, etc. was performed with [this Google Colab notebook][filter_steam_banners] tailored for JPG files.
[![Open In Colab][colab-badge]][filter_steam_banners]

If you wish to further filter banners based on the number of faces visible on the image, see [this notebook][colab-notebook-face-detection] in [`steam-face-detection`][steam-face-detection].
[![Open In Colab][colab-badge]][colab-notebook-face-detection]
This is how I built [the `Steam-OneFace` dataset][steam-oneface-dataset].

NB: original vertical images had already been filtered based on logo filtering, detailed below.
The assumption here is that apps which could not be trusted for their logos should not be trusted for their vertical images.

As of January 9, 2021, [on Google Drive][gdrive-banner-data]:
-   original vertical images (300x450 resolution), available for 29982 out of 48792 games, i.e. 61.4% of games, in `original_vertical_steam_banners.tar` (1.5 GB)

NB: For 2021, the list of appIDs (before any potential filtering) is from [`steam-store-snapshots`][steam-store-snapshots].

### Logos (640x360)

As of September 2020, a selection of logo images is shared [on Google Drive][logos-google-drive]:
-   original logo images (640x360 resolution, PNG files) in [`original_steam_logos_640x360.tar`][logos-original],
-   resized logo images (256x256 resolution, PNG files) in [`resized_steam_logos_256x256.tar`][logos-resized].

Initially, there are 25851 logos out of 45421 games, i.e. 57% of games.

My selection of logo images include 16133 logos, i.e. 62% of logos, after removal of:
-   4420 logos with uncommon bands (anything but RGBA),
-   4117 logos with uncommon resolution (anything but 640x360),
-   726 logos with 100% image space used by content (inconsistent with a logo),
-   455 blank or duplicate logos.

Filtering of duplicates, outliers, etc. was performed with [this Google Colab notebook][filter_steam_logos] tailored for PNG files.
[![Open In Colab][colab-badge]][filter_steam_logos]

**Caveat**: be careful if you use logos, as they are PNG files and feature [a transparent background][transparent-images].

## Screenshots

Steam **screenshots** can be found in [`download-steam-screenshots-data`](https://github.com/woctezuma/download-steam-screenshots-data):
-   original images (inconsistent resolution, at most 600x338),
-   center-cropped and resized images (128x128 resolution).

## References:

-   [Steam Store/Library Asset Specs][steam-asset-specs]
-   [Steam Points Shop Item Specs][points-shop-specs]

<!-- Definitions -->

[download_steam_banners]: <https://colab.research.google.com/github/woctezuma/google-colab/blob/master/download_steam_banners.ipynb>
[filter_steam_logos]: <https://colab.research.google.com/github/woctezuma/google-colab/blob/master/remove_duplicates.ipynb>
[filter_steam_banners]: <https://colab.research.google.com/github/woctezuma/steam-stylegan2-ada/blob/main/remove_duplicates.ipynb>

[steam-face-detection]: <https://github.com/woctezuma/steam-face-detection>
[colab-notebook-face-detection]: <https://colab.research.google.com/github/woctezuma/steam-face-detection/blob/main/detect_faces_on_steam_banners.ipynb>

[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>

[banners-google-drive]: <https://drive.google.com/drive/folders/1bThfr6YOwGr4EZSpv1FoqfhBfY3MfP_t?usp=sharing>
[banners-original]: <https://drive.google.com/file/d/1e57CJogNSPAfw6CZTE1Ht7PvdsqKcGTq/view?usp=sharing>
[banners-filtered]: <https://drive.google.com/file/d/1eI_Qp8DQlzQmXMtNuvbheGM1jCLPgfbr/view?usp=sharing>
[banners-resized]: <https://drive.google.com/file/d/1-7Ni-8CnfdrgB9txGLMvVL_7EUCvgtpZ/view?usp=sharing>
[banners-resized-14k]: <https://drive.google.com/file/d/1v8wmPZTR0DxTvRIjDqduug1pJZo0sLP8/view?usp=sharing>

[gdrive-banner-data]: <https://drive.google.com/drive/folders/1BU8R1JMdzOqc4pzEkpQY6w6FuaretxUH>
[steam-store-snapshots]: <https://github.com/woctezuma/steam-store-snapshots>

[logos-google-drive]: <https://drive.google.com/drive/folders/1_xVdBziq3uIRx53x_s28G7TvTcM5skA1?usp=sharing>
[logos-original]: <https://drive.google.com/file/d/1wNGQyx2rL-mPmPcF8LbbvbFmqH9Zl5RT/view?usp=sharing>
[logos-resized]: <https://drive.google.com/file/d/1-60mEzz4p7vm2kDGHBHIaakrrTe9NzGb/view?usp=sharing>
[transparent-images]: <https://github.com/lucidrains/stylegan2-pytorch#bonus>
[vignetting-wiki]: <https://en.wikipedia.org/wiki/Vignetting>
[steam-oneface-dataset]: <https://github.com/woctezuma/steam-filtered-image-data#steam-oneface-dataset>

[steam-asset-specs]: <https://partner.steamgames.com/doc/store/assets>
[points-shop-specs]: <https://partner.steamgames.com/doc/marketing/pointsshopitems>
