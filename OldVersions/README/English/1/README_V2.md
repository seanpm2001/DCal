
***


# `*.dcal` format specification <img src="/CalendarIcon_Sample1.png" width="100px;" height="100px;" alt=""/><br>

This file is under construction. It may not seem tidy at the moment. Subesequent updates will fix this.

## Description

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

🗓️📅️📆️ DCal is an advanced calendar format that adds significant amounts of customization and control to digital calendars. Inspired by the ICS format, and ProtonCalendar, along with real life calendars.

</details>

## Notes

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not compatible with 8:3 file systems, so not compatible with Windows 3.1/Windows NT 3.51 and below. Nobody should be using these as their daily devices anyways, unless you are using a virtua machine

- This format is not specific to DCalendar, I am hoping to make this an open standard that will work in all modern calendar software.

</details>

## Pronunciation

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Dcal pronunciation: Decal, although I have no rules on pronunciation, this is just the way I pronounce it

See: [:octocat: seanpm2001/Pronunciation](https://github.com/seanpm2001/Pronunciation/)

</details>

## Structure sample alpha 1

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Alpha 1 build of the file structure.

<details><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

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

</details>

The calendar can be different depending on the defined calendar type. The following example will use the Gregorian calendar

<details><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

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

</details>

</details>

***

## Specification

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

THe current DCal specification is planned to be written in Python, JavaScript, and TypeScript.

</details>

***

## Implementation

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

The current DCal implementation is planned to be written in D, and is known as [:octocat: DCalendar](https://github.com/seanpm2001/DCalendar/)

</details>

***

## Media support

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

### Images

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

You can embed images into the cover of the calendar for each individual month/year/century/millennium, and you can also embed images into the description of each event. The following image formats are currently supported: PNG, SVG, JPG, JPEG, JIF, GIF, JFIF, JP2, JPE, WebP, NetP, HEIF, HEIC, HEIFS, HEICS, TIF, TIFF, BMP, DIB, PSD, and GIF. More formats will be supported in the future.

The calendar distributor can impose a limit of the overall image size that can be applied at a per month, per year, and/or per-decade basis. Users who download their calendar files can change this for their personal use.

The heading looks like this

```xml
<img-quota>
    <images>
        <monthly-limit="none">
        <yearly-limit="100000000 bytes"> <!-- Distributors can set the limit to whatever they want, but are advised to take caution, as it can use up lots of space !-->
        <decade-limit="200000000 bytes">   
    </images>
</img-quota>
```

This heading is defined at the beginning of the file.

</details>

### Videos

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Videos can be embedded into the clover of the calendar for each individual month/year/century/millennium, and you can also embed videos into the description of each event. One must take extreme caution doing this, as not only will it take up lots of space, it will be a strain on the CPU and bandwidth. The current video formats are currently supported: AVI, MKV, WebM, NetV, MP4, 3GP, 3GPP, GIFV, MOV, WMV, and QT. More formats will be supported in the future.

Just like with images, the calendar distributor can impose a limit of the overall video size that can be applied at a per month, per year, and/or per-decade basis. Users who download their calendar files can change this for their personal use.

The heading looks like this

```xml
<vid-quota>
    <videos>
        <monthly-limit="none">
        <yearly-limit="1000000000 bytes"> <!-- Distributors can set the limit to whatever they want, but are advised to take caution, as it can use up lots of space !-->
        <decade-limit="2000000000 bytes">   
    </videos>
</vid-quota>
```

This heading is defined at the beginning of the file.

</details>

</details>

***

## Animations

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

### Calendar flip direction

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

The direction of calendar flipping can be changed:

- up and right
- up and left
- down and right
- down and left

This can be defined in the calendar heading like so:

```xml
<animation>
    <flip-direction="Up and left"></flip-direction>
</animation>
```

If you define left instead of right, the calendar may seem like it is going the wrong direction.

<!-- - right to left
- left to right !-->

</details>

### Paper physics

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Paper physics can be enabled (this example builds off of the above example)

```xml
<animation>
    <flip-direction="Up and left"></flip-direction>
    <physics-mode="Paper"></physics-mode>
</animation>
```

</details>

### Coffee spill

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

An Easter Egg known as Coffee Spill is included. It is currently in planning, but the general concept is that you can temporarily stain your calendar with coffee or another beverage by triggering the coffee spill easter egg.

</details>

</details>

***

## DCal metadata

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

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

</details>

***

## Event Timer

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

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

</details>

***

## Demo calendars

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

NTS: For demo purposes: create the following sample calendars:

#### Ab urbe condita calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Armenian Calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Assyrian Calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Baháʼí calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Balinese saka calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Bengali calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Berber calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### British Regnal year

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Buddhist calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Burmese calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Byzantine calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Chinese Calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Coptic calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Discordian calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Ethiopian calendar

- Not enough time to add right now

#### Gregorian

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Gregorian_Simple_Sample1Demo1.dcal

> A simple Gregorian calendar with a range of 1000 CE to 2024 CE

Gregorian_Simple_Sample2Demo1.dcal

> A simple Gregorian calendar with a range of 10000 BCE to 2024 CE

Gregorian_Simple_Sample3Demo1.dcal

> A simple Gregorian calendar with a range of 10000 BCE to 2024 CE

> Also includes a calendar cover, and an image for each month.

</details>

#### Hebrew calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Hindu Calendar: Vikram Samvat

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Hindu Calendar: Shaka Samvat

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Hindu Calendar: Kali Yuga

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Holocene calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Igbo calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Iranian calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Islamic calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Japanese calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Javanese calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Julian

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Juche

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Juche_Simple_Sample1Demo1.dcal

> North Korean calendar (full range) from Juche 1 (Gregorian: 1912) to Juche 112 (Gregorian: 2023)

Juche_Simple_Sample2Demo1.dcal

> North Korean calendar (full range) from Juche 1 (Gregorian: 1912) to Juche 112 (Gregorian: 2023)

> Also includes a calendar cover, and an image for each month.

Juche calendar	111

</details>

#### Julian calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Korean calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Minguo calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Nanakshahi calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Thai solar calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### Tibetan calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

#### UNIX time calendar

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Not enough time to add right now

</details>

***

## Import/Export tool

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Import ICS file
- Export to ICS file (will strip out many features if they are in use)
- Export as DCal
- Export as DCalB (bundle)

</details>

***

## Macros

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

Macros help automate the configuration, organization, and maintenance of a calendar.

Macros can be written in:

- VBScript
- VB.NET
- Other language (not yet defined)

Macro files carry the `.dcalm` file extension.

</details>

***

## Bundles

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

You can bundle multiple calendars into one with  a bundle file. Bundle files carry the `.dcalb` file extension.

</details>

***

## Sample macros

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

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

</details>

***

## Planned platforms

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- [x] DCalendar
- [ ] ProtonMail
- [ ] Outlook
- [ ] Other

</details>

***

## Version control

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

DCal will contain version control functionality via Git. This feature can be disabled, but it isn't recommended, unless the version control system is causing problems. The operating systems backup functionality will be separate from the version control system.

</details>

***

## Time travel

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

With time travel, you can view your calendar at any point in time, without changing your operating systems time/date.

</details>

***

## Extras

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

### Fun things you can do

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

- Turn your calendar into a flipbook
- Add another example here

</details>

</details>

***

### File info

<details open><summary><p lang="en"><b><u>Click/tap here to expand/collapse this section</u></b></p></summary>

**File type:** `Markdown (*.md *.mkd *.mdown *.markdown)`

**File version:** `2 (2023, Monday, January 2nd at 7:59 pm PST)`

**Line count (including blank lines and compiler line):** `979`

**Current article language:** `English (EN_USA)` / `Markdown (CommonMark)` / `HTML5 (HyperText Markup Language 5.3)`

**Encoding:** `UTF-8 (Emoji 12.0 or higher recommended)`

**All times are UTC-7 (PDT/Pacific Time)** `(Please also account for DST (Daylight Savings Time) for older/newer entries up until it is abolished/no longer followed)`

_Note that on 2022, Sunday, March 13th at 2:00 am PST, the time jumped ahead 1 hour to 3:00 am._

**You may need special rendering support for the `<details>` HTML tag being used in this document**

</details>

***

## File history

<details><summary><p lang="en"><b>Click/tap here to expand/collapse the file history section for this project</b></p></summary>

<details><summary><p lang="en"><b>Version 1 (2023, Sunday, January 1st at 5:40 pm PST)</b></p></summary>

**This version was made by:** [`@seanpm2001`](https://github.com/seanpm2001/)

> Changes:

- [x] Started the file
- [x] Added the title section
- [x] Added the `Description` section
- [x] Added the `Notes` section
- [x] Added the `Pronunciation` section
- [x] Added the `Structure sample alpha 1` section
- [x] Added the `DCal Metadata` section
- [x] Added the `Event timer` section
- [x] Added the `Demo calendars` section
- - [x] Added the `Ab urbe condita calendar` subsection
- - [x] Added the `Armenian Calendar` subsection
- - [x] Added the `Assyrian Calendar` subsection
- - [x] Added the `Baháʼí calendar` subsection
- - [x] Added the `Balinese saka calendar` subsection
- - [x] Added the `Bengali calendar` subsection
- - [x] Added the `Berber calendar` subsection
- - [x] Added the `British Regnal year` subsection
- - [x] Added the `Buddhist calendar` subsection
- - [x] Added the `Burmese calendar` subsection
- - [x] Added the `Byzantine calendar` subsection
- - [x] Added the `Chinese Calendar` subsection
- - [x] Added the `Coptic calendar` subsection
- - [x] Added the `Discordian calendar` subsection
- - [x] Added the `Ethiopian calendar` subsection
- - [x] Added the `Gregorian calendar` subsection
- - [x] Added the `Hebrew calendar` subsection
- - [x] Added the `Hindu Calendar: Vikram Samvat` subsection
- - [x] Added the `Hindu Calendar: Shaka Samvat` subsection
- - [x] Added the `Hindu Calendar: Kali Yuga` subsection
- - [x] Added the `Holocene calendar` subsection
- - [x] Added the `Igbo calendar` subsection
- - [x] Added the `Iranian calendar` subsection
- - [x] Added the `Islamic calendar` subsection
- - [x] Added the `Japanese calendar` subsection
- - [x] Added the `Javanese calendar` subsection
- - [x] Added the `Julian` subsection
- - [x] Added the `Juche` subsection
- - [x] Added the `Julian calendar` subsection
- - [x] Added the `Korean calendar` subsection
- - [x] Added the ` Minguo calendar` subsection
- - [x] Added the `Nanakshahi calendar` subsection
- - [x] Added the `Thai solar calendar` subsection
- - [x] Added the `Tibetan calendar` subsection
- - [x] Added the `UNIX time calendar` subsection
- [x] Added the `Import/export tool` section
- [x] Added the `Macros` section
- [x] Added the `Bundles` section
- [x] Added the `Sample macros` section
- [x] Added the `Planned platforms` section
- [x] Added the `file version` section
- [ ] No other changes in version 1

</details>

<details><summary><p lang="en"><b>Version 2 (2023, Monday, January 2nd at 7:59 pm PST)</b></p></summary>

**This version was made by:** [`@seanpm2001`](https://github.com/seanpm2001/)

> Changes:

- [x] Turned every section into a dropdown
- [x] Updated the `Pronunciation` section
- [x] Updated the title section to include the projects stock logo
- [x] Added the `Specification` section
- [x] Added the `Implementation` section
- [x] Added the `media support` section
- - [x] Added the `Images` subsection
- - [x] Added the `Videos` subsection
- [x] Added the `Animations` section
- - [x] Added the `Calendar flip direction` subsection
- - [x] Added the `Paper physics` subsection
- - [x] Added the `Cofee spill` subsection
- [x] Added the `Version control` section
- [x] Added the `Time travel` section
- [x] Added the `Extras` section
- - [x] Added the `Fun things you can do` subsection
- [x] Removed the `File version` footer, and replaced it with a file info section
- [x] Added the `file info` section
- - [x] Added the version number
- - [x] Added the version date
- - [x] Added the line count
- [x] Added the `file history` section
- - [x] Added an entry for version 1
- - [x] Added an entry for version 2
- [ ] No other changes in version 2

</details>

</details>

***
