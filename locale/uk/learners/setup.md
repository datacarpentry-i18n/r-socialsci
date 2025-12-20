---
title: Налаштування
---

## Інструкції з налаштування

**R** and **RStudio** are separate downloads and installations. R — це базове середовище для статистичних обчислень, але працювати лише з R не дуже зручно. RStudio — це графічне інтегроване середовище розробки (IDE), яке робить роботу з R значно простішою та більш інтерактивною. Перед встановленням RStudio необхідно встановити R. Once installed, because RStudio is an IDE, RStudio will run R in
the background.  Окремо запускати R не потрібно.

Після встановлення обох програм вам потрібно встановити пакет **`tidyverse`** безпосередньо з RStudio. The
**`tidyverse`** package is a powerful collection of data science tools within **R**
see the [**`tidyverse`** website](https://tidyverse.tidyverse.org) for more details.
Дотримуйтесь інструкцій нижче для вашої операційної системи, а потім виконайте інструкції зі встановлення **`tidyverse`**.

### Windows

#### If you already have R and RStudio installed

- Відкрийте RStudio та натисніть “Help” > “Check for updates”. Якщо доступна нова версія, закрийте RStudio та завантажте найновішу версію RStudio.
- Щоб перевірити, яку версію R ви використовуєте, запустіть RStudio — версія R буде показана в першому повідомленні в консолі. Або ж ви можете ввести `sessionInfo()`, що також покаже версію R, яку ви використовуєте. Перейдіть на [сайт CRAN](https://cran.r-project.org/bin/windows/base/) і перевірте, чи доступна новіша версія. Якщо так, ви можете оновити R за допомогою пакета `installr`, виконавши:

```r
if( !("installr" %in% installed.packages()) ){install.packages("installr")}
installr::updateR(TRUE)
```

#### Якщо у вас не встановлено R та RStudio

- Завантажте R з
  [сайту CRAN](http://cran.r-project.org/bin/windows/base/release.htm).
- Запустіть файл `.exe`, який був щойно завантажений.
- Перейдіть на [сторінку завантаження RStudio](https://posit.co/download/rstudio-desktop/).
- У розділі _Installers_ виберіть **RStudio x.yy.zzz - Windows.
  Vista/7/8/10** (де x, y та z — номери версій).
- Double click the file to install it.
- Після встановлення відкрийте RStudio, щоб переконатися, що він працює коректно і не з’являються повідомлення про помилки.

### macOS

#### If you already have R and RStudio installed

- Відкрийте RStudio та натисніть “Help” > “Check for updates”. Якщо доступна нова версія, закрийте RStudio та завантажте найновішу версію RStudio.
- Щоб перевірити, яку версію R ви використовуєте, запустіть RStudio — версія R буде показана в першому повідомленні в консолі. Або ж ви можете ввести `sessionInfo()`, що також покаже версію R, яку ви використовуєте. Перейдіть на [сайт CRAN](https://cran.r-project.org/bin/macosx/) і перевірте, чи доступна новіша версія. If so, please download and install
  it. In any case, make sure you have at least R 3.2.

#### Якщо у вас не встановлено R та RStudio

- Завантажте R з
  [сайту CRAN](http://cran.r-project.org/bin/macosx/).
- Виберіть файл '.pkg' для останньої версії R.
- Двічі клацніть на завантаженому файлі для встановлення R.
- It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed
  by some packages).
- Перейдіть на [сторінку завантаження RStudio](https://posit.co/download/rstudio-desktop/).
- У розділі _Installers_ виберіть **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)** (де x, y та z — номери версій).
- Double click the file to install RStudio.
- Після встановлення відкрийте RStudio, щоб переконатися, що він працює коректно і не з’являються повідомлення про помилки.

### Linux

- Дотримуйтесь інструкцій для вашого дистрибутива
  від [CRAN](https://cloud.r-project.org/bin/linux), там наведено інформацію про встановлення найновішої версії R для поширених дистрибутивів. For most
  distributions, you could use your package manager (e.g., for Debian/Ubuntu run
  `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
  don't recommend this approach as the versions provided by this approach are
  usually out of date. У будь-якому разі переконайтеся, що у вас встановлена версія R не нижче 3.2.
- Перейдіть на [сторінку завантаження RStudio](https://posit.co/download/rstudio-desktop/).
- Under _Installers_ select the version that matches your distribution, and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-x.yy.zzz-amd64.deb` at the terminal).
- Після встановлення відкрийте RStudio, щоб переконатися, що він працює коректно і не з’являються повідомлення про помилки.
- Before installing the `tidyverse` package, **Ubuntu** (and related) users may
  need to install the following dependencies: `libcurl4-openssl-dev libssl-dev libxml2-dev`
  (e.g. `sudo apt install libcurl4-openssl-dev libssl-dev libxml2-dev`).

### For everyone

**After installing R and RStudio, you need to install the `tidyverse` and `here` packages.**

- After starting RStudio, at the console type:
  `install.packages("tidyverse")` followed by the enter key. Once this has installed, type
  `install.packages("here")` followed by the enter key. Обидва пакети тепер повинні бути встановлені.

- For reference, the lesson uses `SAFI_clean.csv`. Пряме посилання для завантаження
  цього файлу: [https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI_clean.csv](https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI_clean.csv).
  Ці дані є дещо очищеною версією результатів опитування SAFI Survey Results, доступних на [figshare](https://figshare.com/articles/dataset/SAFI_Survey_Results/6262019).
  Instructions for downloading the data with R are provided in the
  [Before we start episode](https://datacarpentry.org/r-socialsci/00-intro.html).

- The [json episode](https://datacarpentry.org/r-socialsci/07-json.html) uses
  `SAFI.json`. The file is available on GitHub
  [here](https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI.json).


