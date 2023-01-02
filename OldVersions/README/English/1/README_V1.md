
***

# `*.dcal` format specification

This file is under construction. It may not seem tidy at the moment. Subesequent updates will fix this.

## Description

🗓️📅️📆️ DCal is an advanced calendar format that adds significant amounts of customization and control to digital calendars. Inspired by the ICS format, and ProtonCalendar, along with real life calendars.

## Notes

- Not compatible with 8:3 file systems, so not compatible with Windows 3.1/Windows NT 3.51 and below. Nobody should be using these as their daily devices anyways, unless you are using a virtua machine

- This format is not specific to DCalendar, I am hoping to make this an open standard that will work in all modern calendar software.

## Pronunciation

Dcal pronunciation: Decal, although I have no rules on pronunciation, this is just the way I pronounce it

## Structure sample alpha 1

Alpha 1 build of the file structure.

```xml
<header>
Cover font <set a font>
Millennium font <set a font>
Century font <set a font>
Decade font <set a font>
Year font <set a font>
January font: <set a font>
February font: <set a font>
March font: <set a font>
April font: <set a font>
May font: <set a font>
June font: <set a font>
July font: <set a font>
August font: <set a font>
September font: <set a font>
October font: <set a font>
November font: <set a font>
October font: <set a font>
Y-M-D
M-D-Y
D-M-Y
M-Y-D
D-Y-M
e.t.c
Start on Saturday
Start on Sunday
Default view: day
Default view: week
Default view: month
Default view: year
Default view: decade
Default view: century
Default view: millennium (not yet available in some calendars)
Enable images
Enable videos
Enable OS integration (such as, a specific event in the calendar can trigger an alarm to go off, etc.)
Lighting (Light, Dark, System default)
Enable page flipping animation
Calendar type (Julian, Gregorian, Hebrew, Solar, etc.)
<wikipedia-sample comment="For the supported calendar types, representing the year 2022">
Gregorian calendar	2022
MMXXII
Ab urbe condita	2775
Armenian calendar	1471
ԹՎ ՌՆՀԱ
Assyrian calendar	6772
Baháʼí calendar	178–179
Balinese saka calendar	1943–1944
Bengali calendar	1429
Berber calendar	2972
British Regnal year	70 Eliz. 2 – 1 Cha. 3
Buddhist calendar	2566
Burmese calendar	1384
Byzantine calendar	7530–7531
Chinese calendar	辛丑年 (Metal Ox)
4718 or 4658
    — to —
壬寅年 (Water Tiger)
4719 or 4659
Coptic calendar	1738–1739
Discordian calendar	3188
Ethiopian calendar	2014–2015
Hebrew calendar	5782–5783
Hindu calendars	
 - Vikram Samvat	2078–2079
 - Shaka Samvat	1943–1944
 - Kali Yuga	5122–5123
Holocene calendar	12022
Igbo calendar	1022–1023
Iranian calendar	1400–1401
Islamic calendar	1443–1444
Japanese calendar	Reiwa 4
(令和４年)
Javanese calendar	1955–1956
Juche calendar	111
Julian calendar	Gregorian minus 13 days
Korean calendar	4355
Minguo calendar	ROC 111
民國111年
Nanakshahi calendar	554
Thai solar calendar	2565
Tibetan calendar	阴金牛年
(female Iron-Ox)
2148 or 1767 or 995
    — to —
阳水虎年
(male Water-Tiger)
2149 or 1768 or 996
Unix time	1640995200 – 1672531199
5 	May 	31 
</wikipedia-sample>
Yes, I do plan to support the Juche calendar, along with other calendars of this magnitude, I will be supporting all calendar formats. People may commonly set their calendar to Juche as a joke, or for historical/research/other purposes, but it will remains an option that won't be removed nonetheless. It isn't that hard to support.
</header>
```

The calendar can be different depending on the defined calendar type. The following example will use the Gregorian calendar

```xml
<cover>
<image>image for once-a-millennium Calendar cover</image>
<image>image for once-a-century Calendar cover</image>
<image>image for once-a-decade Calendar cover</image>
<image>image for yearly Calendar cover</image>
</cover>

<!-- Supported image formats: Any, or: PNG, SVG, JPG, JPEG, JIF, GIF, JFIF, JP2, JPE, WebP, NetP, HEIF, HEIC, HEIFS, HEICS, TIF, TIFF, BMP, DIB, PSD, etc. !-->

<image>image for January</image>
January
1-31

<image>image for February</image>
February
1-28/29

<image>image for March</image>
March
1-31

<image>image for April</image>
March
1-30

<image>image for May</image>
March
1-31

<image>image for June</image>
March
1-30

<image>image for July</image>
March
1-31

<image>image for August</image>
March
1-31

<image>image for September</image>
March
1-30

<image>image for October</image>
March
1-31

<image>image for November</image>
March
1-30

<image>image for December</image>
March
1-31
```

***

## DCal metadata

- Email associations
- Location associations
- Descriptions
- Labels
- Categories
- Actions {
- 1. Trigger a notification
- 2. Trigger an alarm
- 3. Trigger a popup }
- Events

***

## Event Timer

Set a timer for the duration of an event.

- Can't go any lower than 5 seconds
- By 5 seconds
- By 10 seconds
- By 15 seconds
- By 20 seconds
- By 30 seconds
- By minute
- By 2.5 minutes
- By 5 minutes
- By 10 minutes
- By 15 minutes
- By 20 minutes
- By 30 minutes
- By 60 minutes
- By 90 minutes
- By 120 minutes
- By 150 minutes
- By 180 minutes
- By 210 minutes
- By 240 minutes
- By 270 minutes
- By 300 minutes
- By 330 minutes
- By 360 minutes
- By 390 minutes
- By 420 minutes
- By 450 minutes
- By 480 minutes
- By 510 minutes
- By 540 minutes
- By 570 minutes
- By 600 minutes
- By 630 minutes
- By 660 minutes
- By 690 minutes
- By 720 minutes
- By 750 minutes
- By 780 minutes
- By 810 minutes
- By 840 minutes
- By 870 minutes
- By 900 minutes
- By 930 minutes
- By 960 minutes
- By 990 minutes
- By 1020 minutes
- By 1050 minutes
- By 1080 minutes
- By 1110 minutes
- By 1140 minutes
- By 1170 minutes
- By 1200 minutes
- By 1230 minutes
- By 1260 minutes
- By 1290 minutes
- By 1320 minutes
- By 1350 minutes
- By 1380 minutes
- By 1410 minutes
- By 1440 minutes (24 hours)
- All day (a separate category than - By 1440 minutes)

***

## Demo calendars

NTS: For demo purposes: create the following sample calendars:

#### Ab urbe condita calendar

- Not enough time to add right now

#### Armenian Calendar

- Not enough time to add right now

#### Assyrian Calendar

- Not enough time to add right now

#### Baháʼí calendar

- Not enough time to add right now

#### Balinese saka calendar

- Not enough time to add right now

#### Bengali calendar

- Not enough time to add right now

#### Berber calendar

- Not enough time to add right now

#### British Regnal year

- Not enough time to add right now

#### Buddhist calendar

- Not enough time to add right now

#### Burmese calendar

- Not enough time to add right now

#### Byzantine calendar

- Not enough time to add right now

#### Chinese Calendar

- Not enough time to add right now

#### Coptic calendar

- Not enough time to add right now

#### Discordian calendar

- Not enough time to add right now

#### Ethiopian calendar

- Not enough time to add right now

#### Gregorian

Gregorian_Simple_Sample1Demo1.dcal

> A simple Gregorian calendar with a range of 1000 CE to 2024 CE

Gregorian_Simple_Sample2Demo1.dcal

> A simple Gregorian calendar with a range of 10000 BCE to 2024 CE

Gregorian_Simple_Sample3Demo1.dcal

> A simple Gregorian calendar with a range of 10000 BCE to 2024 CE

> Also includes a calendar cover, and an image for each month.

#### Hebrew calendar

- Not enough time to add right now

#### Hindu Calendar: Vikram Samvat

- Not enough time to add right now

#### Hindu Calendar: Shaka Samvat

- Not enough time to add right now

#### Hindu Calendar: Kali Yuga

- Not enough time to add right now

#### Holocene calendar

- Not enough time to add right now

#### Igbo calendar

- Not enough time to add right now

#### Iranian calendar

- Not enough time to add right now

#### Islamic calendar

- Not enough time to add right now

#### Japanese calendar

- Not enough time to add right now

#### Javanese calendar

- Not enough time to add right now

#### Julian

- Not enough time to add right now

#### Juche

Juche_Simple_Sample1Demo1.dcal

> North Korean calendar (full range) from Juche 1 (Gregorian: 1912) to Juche 112 (Gregorian: 2023)

Juche_Simple_Sample2Demo1.dcal

> North Korean calendar (full range) from Juche 1 (Gregorian: 1912) to Juche 112 (Gregorian: 2023)

> Also includes a calendar cover, and an image for each month.

Juche calendar	111

#### Julian calendar

- Not enough time to add right now

#### Korean calendar

- Not enough time to add right now

#### Minguo calendar

- Not enough time to add right now

#### Nanakshahi calendar

- Not enough time to add right now

#### Thai solar calendar

- Not enough time to add right now

#### Tibetan calendar

- Not enough time to add right now

#### UNIX time calendar

- Not enough time to add right now

***

## Import/Export tool

- Import ICS file
- Export to ICS file (will strip out many features if they are in use)
- Export as DCal
- Export as DCalB (bundle)

***

## Macros

Macros help automate the configuration, organization, and maintenance of a calendar.

Macros can be written in:

- VBScript
- VB.NET
- Other language (not yet defined)

Macro files carry the `.dcalm` file extension.

***

## Bundles

You can bundle multiple calendars into one with  a bundle file. Bundle files carry the `.dcalb` file extension.

***

## Sample macros

Included macros

- Birthdays.dcalm
- Is-Was.dcalm
- Daily-tasks.dcalm
- American-Holidays.dcalm
- American-History.dcalm
- Religious-Holidays_Christianity.dcalm
- Religious-Holidays_Hinduism.dcalm
- Religious-Holidays_Judaism.dcalm
- Religious-Holidays_Islam.dcalm
- More coming soon

***

## Planned platforms

- [x] DCalendar
- [ ] ProtonMail
- [ ] Outlook
- [ ] Other

***

**File version:** `1 (2023, Sunday, January 1st at 5:40 pm PST)`

***
