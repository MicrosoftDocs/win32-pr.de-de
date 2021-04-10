---
title: Zuordnung von RSS-Feeds zu Windows Media Device Manager-Eigenschaften
description: Zuordnung von RSS-Feeds zu Windows Media Device Manager-Eigenschaften
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Device Manager, RSS-Feeds
- Device Manager, RSS-Feeds
- Programmier Handbuch, RSS-Feeds
- Desktop Anwendungen, RSS-Feeds
- Erstellen von Windows Media Device Manager-Anwendungen, RSS-Feeds
- RSS-Feeds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855572"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Zuordnung von RSS-Feeds zu Windows Media Device Manager-Eigenschaften

Windows Media Player 11 stellt eine RSS-Aggregator-Funktion bereit, die es Benutzern ermöglicht, Inhalte aus Podcasts auf ihren Computern zu speichern. In diesem Thema werden die in einem RSS-Feed gefundenen XML-Elemente beschrieben. Außerdem werden diese RSS-Elemente den Windows Media Device Manager-Eigenschaften zugeordnet.

Die Elemente in einem RSS-Feed verfügen über die folgende Hierarchie und Attribute:


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



In der folgenden Tabelle sind die Channelelemente in einem RSS-Feed und die entsprechenden Eigenschaften des Windows Media-Device Manager aufgeführt.



| Channel-Element | Status         | Zugehörige Windows Media Device Manager-Eigenschaft   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Optional       | [g \_ wszwmdmgenre](metadata-constants.md)             |
| cloud           | Nicht verfügbar | Nicht verfügbar                                        |
| Copyright       | Optional       | [g \_ wszwmdmprovidercopyright](metadata-constants.md) |
| description     | Erforderlich       | [g \_ wszwmdmdescription](metadata-constants.md)       |
| Docs            | Nicht verfügbar | Nicht verfügbar                                        |
| Generator       | Nicht verfügbar | Nicht verfügbar                                        |
| language        | Nicht verfügbar | Nicht verfügbar                                        |
| lastBuildDate   | Optional       | [g \_ wszwmdmlastmodifieddate](metadata-constants.md)  |
| link            | Erforderlich       | [g \_ wszwmdmdestinationurl](metadata-constants.md)    |
| managingEditor  | Optional       | [g \_ wszwmdmeditor](metadata-constants.md)            |
| pubDate         | Optional       | [g \_ wszwmdmyear](metadata-constants.md)              |
| rating          | Nicht verfügbar | Nicht verfügbar                                        |
| skipdays        | Nicht verfügbar | Nicht verfügbar                                        |
| skiphours       | Nicht verfügbar | Nicht verfügbar                                        |
| TextInput       | Nicht verfügbar | Nicht verfügbar                                        |
| title           | Erforderlich       | [g \_ wszwmdmtitle](metadata-constants.md)             |
| ttl             | Optional       | [g \_ wszwmdmtimeeslive](metadata-constants.md)        |
| webMaster       | Optional       | [g \_ wszwmdmwebmaster](metadata-constants.md)         |



 

In der folgenden Tabelle sind die Bildelemente in einem RSS-Feed und die entsprechenden WMDM-Eigenschaften aufgeführt.



| Image-Element | Status   | Zugehörige Windows Media Device Manager-Eigenschaft |
|---------------|----------|-----------------------------------------------------|
| description   | Optional | [g \_ wszwmdmdescription](metadata-constants.md)     |
| height        | Optional | [g \_ wszwmdmheight](metadata-constants.md)          |
| link          | Optional | [g \_ wszwmdmdestinationurl](metadata-constants.md)  |
| title         | Optional | [g \_ wszwmdmtitle](metadata-constants.md)           |
| url           | Optional | [g \_ wszwmdmsourceurl](metadata-constants.md)       |
| width         | Optional | [g \_ wszwmdmwidth](metadata-constants.md)           |



 

In der folgenden Tabelle sind die Element Elemente in einem RSS-Feed und die entsprechenden Eigenschaften des Windows Media-Device Manager aufgeführt.



| Item-Element | Attribut   | Status         | Zugehörige Windows Media Device Manager-Eigenschaft            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| author       |             | Optional       | [g \_ wszwmdmauthor](metadata-constants.md)                     |
| category     |             | Optional       | [g \_ wszwmdmgenre](metadata-constants.md)                      |
|              | Domäne      | Nicht verfügbar | Nicht verfügbar                                                 |
| description  |             | Optional       | [g \_ wszwmdmdescription](metadata-constants.md)                |
| ungs    |             | Optional       | Nicht verfügbar                                                 |
|              | length      | Erforderlich       | [g \_ wszwmdmfilesize](metadata-constants.md)                   |
|              | type        | Erforderlich       | (Der MIME-Typ sollte dem Eigenschafts Inhaltstyp zugeordnet werden.) |
|              | url         | Erforderlich       | [g \_ wszwmdmsourceurl](metadata-constants.md)                  |
| guid         |             | Optional       | [g \_ wszwmdmediaguid](metadata-constants.md)                   |
|              | ispermalink | Nicht verfügbar | Nicht verfügbar                                                 |
| link         |             | Optional       | [g \_ wszwmdmdestinationurl](metadata-constants.md)             |
| pubDate      |             | Optional       | [g \_ wszwmdmyear](metadata-constants.md)                       |
| source       |             | Nicht verfügbar | Nicht verfügbar                                                 |
| title        |             | Optional       | [g \_ wszwmdmtitle](metadata-constants.md)                      |



 

Beispiel

Das folgende Beispiel zeigt einen kompletten RSS-Feed für einen fiktiven Podcast, der vom CEO eines Veröffentlichungs Unternehmens bereitgestellt wird.


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



Zuordnung von RSS-Channel-Elementen zu Windows Media Device Manager-Eigenschafts Werten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-channelelementen im vorherigen Beispiel bestimmten Windows Media Device Manager-Eigenschaften zugeordnet werden.



| Windows Media Device Manager-Eigenschaft                    | Wert                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszwmdmauthordate](metadata-constants.md)           | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [g \_ wszwmdmdescription](metadata-constants.md)          | Lucerne Publishing CEO Peter Bankow befasst sich mit den neuesten Trends in Online Veröffentlichungen. |
| [g \_ wszwmdmdestination- \_ URL](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszwmdmeditor](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszwmdmfilekreationdate](metadata-constants.md)     | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [g \_ wszwmdmfilename](metadata-constants.md)             | Die digitale Veröffentlichung                                                                       |
| [g \_ wszwmdmfilesize](metadata-constants.md)             | 13.790                                                                                        |
| [g \_ wszwmdmformatcode](metadata-constants.md)           | WMDM- \_ Formatcode- \_ Medien Umwandlung \_                                                                 |
| [g \_ wszwmdmgenre](metadata-constants.md)                | News                                                                                          |
| [g \_ wszwmdmlast-Änderungs \_ \_ Datum](metadata-constants.md) | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [g \_ wszwmdmlastmodifieddate](metadata-constants.md)     | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [g \_ wszwmdmprovidercopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. Alle Rechte vorbehalten.                                        |
| [g \_ wszwmdmtimeeslive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszwmdmtitle](metadata-constants.md)                | Die digitale Veröffentlichung                                                                       |
| [g \_ wszwmdmwebmaster](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszwmdmyear](metadata-constants.md)                 | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |



 

Zuordnung von RSS-Bildelementen zu Windows Media Device Manager-Eigenschafts Werten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Bildelementen im vorherigen Beispiel bestimmten Windows Media Device Manager-Eigenschaften zugeordnet werden.



| Windows Media Device Manager-Eigenschaft                | Wert                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszwmdmalbumcoverformat](metadata-constants.md) | WPD- \_ Objekt \_ Format \_ GIF                         |
| [g \_ wszwmdmalbumcoversize](metadata-constants.md)   | 512                                              |
| [g \_ wszwmdmdescription](metadata-constants.md)      | Lucerne-Logo                                     |
| [g \_ wszwmdmdestinationurl](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszwmdmheight](metadata-constants.md)           | 300                                              |
| [g \_ wszwmdmsourceurl](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszwmdmtitle](metadata-constants.md)            | Lucerne Publishing                               |
| [g \_ wszwmdmwidth](metadata-constants.md)            | 300                                              |



 

Zuordnung von RSS-Element Elementen zu Windows Media Device Manager-Eigenschafts Werten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Element Elementen im vorherigen Beispiel bestimmten Windows Media Device Manager-Eigenschaften zugeordnet werden.



| Windows Media Device Manager-Eigenschaft                | Wert                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszwmdmauthor](metadata-constants.md)           | Luzerner                                                                                                                             |
| [g \_ wszwmdmauthordate](metadata-constants.md)       | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                      |
| [g \_ wszwmdmdescription](metadata-constants.md)      | Online Veröffentlichungen werden rasch geändert. Ein Publishing House-CEO untersucht die Trends der letzten fünf Jahre und deren Auswirkungen. |
| [g \_ wszwmdmdestinationurl](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszwmdmduration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszwmdmfilekreationdate](metadata-constants.md) | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                      |
| [g \_ wszwmdmfilesize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszwmdmformatcode](metadata-constants.md)       | WMDM \_ Formatcode \_ MP3                                                                                                               |
| [g \_ wszwmdmgenre](metadata-constants.md)            | News                                                                                                                                |
| [g \_ wszwmdmlastmodifieddate](metadata-constants.md) | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                      |
| [g \_ wszwmdmmediaguid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszwmdmsourceurl](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszwmdmtitle](metadata-constants.md)            | Die digitale Veröffentlichung                                                                                                             |
| [g \_ wszwmdmyear](metadata-constants.md)             | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metadatenkonstanten**](metadata-constants.md)
</dt> </dl>

 

 




