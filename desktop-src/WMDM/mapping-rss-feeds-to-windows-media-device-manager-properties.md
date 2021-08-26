---
title: Zuordnen von RSS-Feeds zu Windows Medieneigenschaften Geräte-Manager
description: Zuordnen von RSS-Feeds zu Windows Medieneigenschaften Geräte-Manager
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Medien Geräte-Manager, RSS-Feeds
- Geräte-Manager,RSS-Feeds
- Programmierhandbuch, RSS-Feeds
- Desktopanwendungen, RSS-Feeds
- Erstellen von Windows Media Geräte-Manager-Anwendungen, RSS-Feeds
- RSS-Feeds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355515217db31740603d5c6323ef8455da4b29ee80bec508897d2d4df5d59bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031680"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Zuordnen von RSS-Feeds zu Windows Medieneigenschaften Geräte-Manager

Windows Media Player 11 bietet ein RSS-Aggregatorfeature, mit dem Benutzer Inhalte aus Podcasts auf ihren Computern speichern können. In diesem Thema werden die XML-Elemente in einem RSS-Feed beschrieben. Darüber hinaus werden diese RSS-Elemente Windows Media Geräte-Manager-Eigenschaften zugeordnet.

Die Elemente in einem RSS-Feed weisen die folgende Hierarchie und die folgenden Attribute auf:


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



In der folgenden Tabelle sind die Kanalelemente in einem RSS-Feed und die entsprechenden Windows Media Geräte-Manager-Eigenschaften aufgeführt.



| Channel-Element | Status         | Entsprechende Windows Media Geräte-Manager-Eigenschaft   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Optional       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| cloud           | Nicht verfügbar | Nicht verfügbar                                        |
| Copyright       | Optional       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| description     | Erforderlich       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| Docs            | Nicht verfügbar | Nicht verfügbar                                        |
| Generator       | Nicht verfügbar | Nicht verfügbar                                        |
| language        | Nicht verfügbar | Nicht verfügbar                                        |
| lastBuildDate   | Optional       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | Erforderlich       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | Optional       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| Pubdate         | Optional       | [g \_ wszWMDMYear](metadata-constants.md)              |
| rating          | Nicht verfügbar | Nicht verfügbar                                        |
| skipDays        | Nicht verfügbar | Nicht verfügbar                                        |
| skipHours       | Nicht verfügbar | Nicht verfügbar                                        |
| Textinput       | Nicht verfügbar | Nicht verfügbar                                        |
| title           | Erforderlich       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Optional       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| Webmaster       | Optional       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

In der folgenden Tabelle sind die Bildelemente in einem RSS-Feed und die entsprechenden WMDM-Eigenschaften aufgeführt.



| Image-Element | Status   | Entsprechende Windows Media Geräte-Manager-Eigenschaft |
|---------------|----------|-----------------------------------------------------|
| description   | Optional | [g \_ wszWMDMDescription](metadata-constants.md)     |
| height        | Optional | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | Optional | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| title         | Optional | [g \_ wszWMDMTitle](metadata-constants.md)           |
| URL           | Optional | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Optional | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

In der folgenden Tabelle sind die Elementelemente in einem RSS-Feed und die entsprechenden Windows Media Geräte-Manager-Eigenschaften aufgeführt.



| Item-Element | attribute   | Status         | Entsprechende Windows Media Geräte-Manager-Eigenschaft            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| author       |             | Optional       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Optional       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | Domäne      | Nicht verfügbar | Nicht verfügbar                                                 |
| description  |             | Optional       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| Gehäuse    |             | Optional       | Nicht verfügbar                                                 |
|              | length      | Erforderlich       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Erforderlich       | (Der MIME-Typ sollte dem Inhaltstyp der Eigenschaft zugeordnet werden.) |
|              | URL         | Erforderlich       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Optional       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | isPermaLink | Nicht verfügbar | Nicht verfügbar                                                 |
| link         |             | Optional       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| Pubdate      |             | Optional       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | Nicht verfügbar | Nicht verfügbar                                                 |
| title        |             | Optional       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Beispiel

Das folgende Beispiel zeigt einen vollständigen RSS-Feed für einen fiktiven Podcast, der vom CEO eines Veröffentlichungsunternehmens bereitgestellt wird.


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



Zuordnen von RSS-Kanalelementen zu Windows Media Geräte-Manager-Eigenschaftswerten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Kanalelementen im vorherigen Beispiel bestimmten Eigenschaften Windows Media Geräte-Manager werden.



| Windows Media Geräte-Manager-Eigenschaft                    | Wert                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | Peter Bankov, CEO von Lucerne Publishing, wirf einen Blick auf die neuesten Trends in Onlineveröffentlichungen. |
| [g \_ wszWMDMDESTINATION \_ URL](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | Die digitale Veröffentlichung                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13,790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | WMDM \_ FORMATCODE \_ MEDIA \_ CAST                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | News                                                                                          |
| [g \_ wszWMDMLAST \_ MODIFIED \_ DATE](metadata-constants.md) | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. Alle Rechte vorbehalten.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | Die digitale Veröffentlichung                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |



 

Zuordnen von RSS-Bildelementen zu Windows Media Geräte-Manager-Eigenschaftswerten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Bildelementen im vorherigen Beispiel bestimmten Eigenschaften Windows Media Geräte-Manager werden.



| Windows Media Geräte-Manager-Eigenschaft                | Wert                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMWiederherstellenFormat](metadata-constants.md) | \_WPD-OBJEKTFORMAT \_ \_ GIF                         |
| [g \_ wszWMDMWiederherstellenSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Lucerne-Logo                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Lucerne Publishing                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

Zuordnen von RSS-Elementelementen zu Windows Media Geräte-Manager-Eigenschaftswerten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS Item-Elementen im vorherigen Beispiel bestimmten Eigenschaften Windows Media Geräte-Manager werden.



| Windows Media Geräte-Manager-Eigenschaft                | Wert                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Luzern                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Ite, 1. Juni 2006, 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Onlineveröffentlichungen ändern sich schnell. Ein CEO eines Herausgebers untersucht die Trends der letzten fünf Jahre und deren Auswirkungen. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Ite, 1. Juni 2006, 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | WMDM \_ FORMATCODE \_ MP3                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | News                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Ite, 1. Juni 2006, 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Die digitale Veröffentlichung                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Ite, 1. Juni 2006, 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metadatenkonst constants**](metadata-constants.md)
</dt> </dl>

 

 




