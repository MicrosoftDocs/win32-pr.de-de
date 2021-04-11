---
description: WPD \_ - \_ Inhaltstyp \_ Medien Umwandlung \_
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2daafb381aac802b9add130aa97e9750f30e7847
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132201"
---
# <a name="wpd_content_type_media_cast"></a>WPD \_ - \_ Inhaltstyp \_ Medien Umwandlung \_

Ein-Objekt, das den Typ als Medien Umwandlung für den WPD- \_ Inhaltstyp beschreibt, \_ \_ \_ stellt eine Auflistung verwandter Inhalte dar.

Ein Mediacast-Objekt kann als Container Objekt betrachtet werden, das verwandte Inhalte gruppiert, ebenso wie eine Wiedergabeliste Musik gruppiert. Häufig wird ein Mediacast-Objekt verwendet, um Medieninhalte zu gruppieren, die Online veröffentlicht wurden. Beispielsweise kann ein RSS-Kanal als Mediacast-Objekt dargestellt werden, dessen Objekt Verweise auf Inhalts Objekte verweisen, die jedes Element im Kanal darstellen.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Eigenschaftenname**                                                                                                     | **Erforderlich oder optional**                                              |
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich.                                                             |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                             |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                             |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                             |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.               |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                             |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                          |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                             |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                     | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.            |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                             |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                               | Erforderlich, wenn das Objekt gelöscht werden kann.                                |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [Copyright von WPD- \_ Medien \_](media-properties.md)                                                     | Dies ist optional.                                                             |
| [\_ \_ Eltern \_ Bewertung für WPD-Medien](media-properties.md)                                        | Dies ist optional.                                                             |
| [WPD \_ - \_ medienmeta- \_ Genre](media-properties.md)                                                  | Dies ist optional.                                                             |
| [\_ \_ unter \_ Titel der WPD-Medien](media-properties.md)                                                    | Dies ist optional.                                                             |
| [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)                                              | Empfohlen.                                                          |
| [WPD- \_ Medien \_ Titel](media-properties.md)                                                             | Empfohlen.                                                          |
| [WPD- \_ Medien \_ Besitzer](media-properties.md)                                                             | Empfohlen.                                                          |
| [Editor für WPD- \_ Medien \_ Verwaltung \_](media-properties.md)                                        | Empfohlen.                                                          |
| [WPD \_ Media- \_ Webdienste](media-properties.md)                                                     | Empfohlen.                                                          |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                                                  | Empfohlen.                                                          |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)                                        | Empfohlen.                                                          |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                                                 | Dies ist optional.                                                             |
| [WPD- \_ Medien \_ Genre](media-properties.md)                                                             | Dies ist optional.                                                             |
| [Lesezeichen für WPD- \_ Medien \_ Objekt \_](media-properties.md)                                        | Empfohlen                                                           |
| [Datum des \_ \_ letzten \_ Builds \_ für WPD-Medien](media-properties.md)                                       | Empfohlen.                                                          |
| [\_ \_ \_ Lebensdauer von \_ WPD-Medien](media-properties.md)                                             | Dies ist optional.                                                             |
| [\_ \_ unter \_ Beschreibung der WPD-Medien](object-properties.md)                                                                 | Dies ist optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                               | Erforderlich oder optional | BESCHREIBUNG                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md)      | Dies ist optional.            | Enthält die Mediacast-Datei Daten. Wenn diese Mediacast z. b. einen RSS-Kanal darstellt, ist dies möglicherweise das RSS-Dokument. |
| [**WPD- \_ Ressourcen \_ Miniaturansicht**](wpd-resource-thumbnail.md)  | Dies ist optional.            | Enthält die Miniaturansicht, die diese Mediacast darstellt.                                                                         |
| [**WPD- \_ Ressourcen \_ Album- \_ Grafik**](wpd-resource-album-art.md) | Dies ist optional.            | Enthält die Grafik für diese Mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Zuordnung von RSS-Elementen und Mediacast-Eigenschaften

Ein RSS-Kanal kann als ein Mediacast-Objekt dargestellt werden, dessen Verweise auf Inhalts Objekte zeigen, die die einzelnen Elemente in einem bestimmten Kanal darstellen.

Die Elemente in einem RSS-Feed weisen die folgende Hierarchie und Attribute auf.


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



In der folgenden Tabelle werden die Channelelemente in einem RSS-Feed und die entsprechenden Media Cast-Eigenschaften des WPD- \_ Inhalts \_ Typs aufgelistet \_ \_ .



|                     |                          |                                                                                 |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| **Channel-Element** | **RSS-Feed-Anforderung** | **Zugehörige Mediacast-Eigenschaft**                                            |
| category            | Dies ist optional.                | [WPD- \_ Medien \_ Genre](media-properties.md)                       |
| cloud               | Nicht zutreffend          | Nicht zutreffend                                                                 |
| Copyright           | Dies ist optional.                | [Copyright von WPD- \_ Medien \_](media-properties.md)               |
| description         | Erforderlich.                | [WPD- \_ Medien \_ Beschreibung](media-properties.md)           |
| Docs                | Nicht zutreffend          | Nicht zutreffend                                                                 |
| Generator           | Nicht zutreffend          | Nicht zutreffend                                                                 |
| language            | Nicht zutreffend          | Nicht zutreffend                                                                 |
| lastBuildDate       | Dies ist optional.                | [Datum des \_ \_ letzten \_ Builds \_ für WPD-Medien](media-properties.md) |
| link                | Erforderlich.                | [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)  |
| managingEditor      | Dies ist optional.                | [Editor für WPD- \_ Medien \_ Verwaltung \_](media-properties.md)  |
| pubDate             | Dies ist optional.                | [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)        |
| rating              | Nicht zutreffend          | Nicht zutreffend                                                                 |
| skipdays            | Nicht zutreffend          | Nicht zutreffend                                                                 |
| skiphours           | Nicht zutreffend          | Nicht zutreffend                                                                 |
| TextInput           | Nicht zutreffend          | Nicht zutreffend                                                                 |
| title               | Erforderlich.                | [WPD- \_ Objekt \_ Name](object-properties.md)                      |
| ttl                 | Dies ist optional.                | [\_ \_ \_ Lebensdauer von \_ WPD-Medien](media-properties.md)       |
| webMaster           | Dies ist optional.                | [WPD \_ Media- \_ Webdienste](media-properties.md)               |



 

In der folgenden Tabelle werden die Image-Elemente in einem RSS-Feed und die entsprechenden Media Cast-Eigenschaften des WPD- \_ Inhalts \_ Typs aufgelistet \_ \_ .



|                   |                          |                                                                                |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| **Image-Element** | **RSS-Feed-Anforderung** | **Mediacast-Eigenschaft**                                                         |
| description       | Dies ist optional.                | [WPD- \_ Medien \_ Beschreibung](media-properties.md)          |
| height            | Dies ist optional.                | [WPD- \_ Medien \_ Höhe](media-properties.md)                    |
| link              | Dies ist optional.                | [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md) |
| title             | Dies ist optional.                | [WPD- \_ Objekt \_ Name](object-properties.md)                     |
| url               | Dies ist optional.                | [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)           |
| width             | Dies ist optional.                | [WPD- \_ Medien \_ Breite](media-properties.md)                      |



 

In der folgenden Tabelle werden die Element Elemente in einem RSS-Feed und die entsprechenden Media Cast-Eigenschaften für den WPD- \_ \_ Inhaltstyp aufgelistet \_ \_ .



|                  |               |                          |                                                                                |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| **Item-Element** | **Attribut** | **RSS-Feed-Anforderung** | **Mediacast-Eigenschaft**                                                         |
| author           |               | Dies ist optional.                | [WPD- \_ Medien \_ Künstler](media-properties.md)                    |
| category         |               | Dies ist optional.                | [WPD- \_ Medien \_ Genre](media-properties.md)                      |
|                  | Domäne        | Nicht zutreffend          | Nicht zutreffend                                                                |
| description      |               | Dies ist optional.                | [WPD- \_ Medien \_ Beschreibung](media-properties.md)          |
| ungs        |               | Dies ist optional.                |                                                                                |
|                  | url           | Erforderlich.                | [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)           |
|                  | length        | Erforderlich.                | [WPD- \_ Objekt \_ Größe](object-properties.md)                     |
|                  | type          | Erforderlich.                | (Der MIME-Typ sollte dem Eigenschafts Inhaltstyp zugeordnet werden.)                 |
| guid             |               | Dies ist optional.                | [WPD- \_ Medien- \_ GUID](media-properties.md)                        |
|                  | ispermalink   | Nicht zutreffend          | Nicht zutreffend                                                                |
| link             |               | Dies ist optional.                | [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md) |
| pubDate          |               | Dies ist optional.                | [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)       |
| source           |               | Nicht zutreffend          | Nicht zutreffend                                                                |
| title            |               | Dies ist optional.                | [WPD- \_ Objekt \_ Name](object-properties.md)                     |



 

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
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Zuordnung von RSS-Channel-Elementen zu WPD-Eigenschafts Werten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Kanal Elementen im vorherigen Beispiel bestimmten WPD-Eigenschaften zugeordnet werden.



|                                                                                              |                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **WPD-Eigenschaft**                                                                             | **Wert**                                                                                     |
| [Copyright von WPD- \_ Medien \_](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. Alle Rechte vorbehalten.                                        |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                        | Lucerne Publishing CEO Peter Bankow befasst sich mit den neuesten Trends in Online Veröffentlichungen. |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [WPD- \_ Medien \_ Genre](media-properties.md)                                    | News                                                                                          |
| [Datum des \_ \_ letzten \_ Builds \_ für WPD-Medien](media-properties.md)              | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [Editor für WPD- \_ Medien \_ Verwaltung \_](media-properties.md)               | someone@example.com                                                                           |
| [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)                     | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [\_ \_ \_ Lebensdauer von \_ WPD-Medien](media-properties.md)                    | 240                                                                                           |
| [WPD- \_ Medien \_ Titel](media-properties.md)                                    | Die digitale Veröffentlichung                                                                       |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [WPD \_ Media- \_ Webdienste](media-properties.md)                            | someone@example.com                                                                           |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                  | WPD \_ - \_ Inhaltstyp \_ Medien Umwandlung \_                                                               |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                  | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                | Fr, 9. Juni 2006 14:00:28 (EDT)                                                                 |
| [WPD- \_ Objekt \_ Format](object-properties.md)                               | WPD- \_ Objekt \_ Format \_ abstrakte \_ Medien \_ Umwandlung                                                    |
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                       | Von der Sitzung abhängiger Wert.                                                                      |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                   | Die digitale Veröffentlichung                                                                       |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)     | Die digitale Veröffentlichung                                                                       |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                        | Mypodcasts (ein fiktiver Podcast-Ordner auf dem Gerät). Angenommen, für dieses Beispiel lautet der Wert "0A0".        |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md) | Sitzungs unabhängiger Wert. (Für dieses Beispiel wird "0a1" angenommen.)                                   |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                       | 0a2 für N Elemente<br/>                                                                   |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                   | 13.790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Zuordnung von RSS-Bildelementen zu WPD-Eigenschafts Werten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Bildelementen im vorherigen Beispiel bestimmten WPD-Eigenschaften zugeordnet werden.



|                                                                                                                         |                                                     |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **WPD-Eigenschaft**                                                                                                        | **Wert**                                           |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                                                   | Lucerne-Logo                                        |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [WPD- \_ Medien \_ Höhe](media-properties.md)                                                             | 300                                                 |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [WPD- \_ Medien \_ Breite](media-properties.md)                                                               | 300                                                 |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                              | Lucerne Publishing                                  |
| [Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.](attributes.md)                               | Variant \_ true                                       |
| [WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen](attributes.md)                                   | Variant \_ true                                       |
| [WPD- \_ Ressourcen \_ Attribut \_ Format](resource-attribute-properties.md)                     | WPD- \_ Objekt \_ Format \_ GIF                            |
| [WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe](attributes.md) | 1024                                                |
| [Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Zuordnung von RSS-Element Elementen zu WPD-Eigenschafts Werten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Element Elementen im vorherigen Beispiel bestimmten WPD-Eigenschaften zugeordnet werden.



|                                                                                              |                                                                                                                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **WPD-Eigenschaft**<br/>                                                                  | **Wert**                                                                                                                        |
| [WPD- \_ Medien \_ Titel](media-properties.md)                                    | Die digitale Veröffentlichung                                                                                                          |
| [Dauer der WPD- \_ Medien \_](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD- \_ Medien \_ Künstler](media-properties.md)                                  | Luzerner                                                                                                                          |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                        | Online Veröffentlichungen werden rasch geändert. Ein Publishing House-CEO untersucht die Trends der letzten fünf Jahre und deren Auswirkungen. |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [WPD- \_ Medien \_ Genre](media-properties.md)                                    | News                                                                                                                             |
| [WPD- \_ Medien- \_ GUID](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)                     | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                   |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)            | 0a1                                                                                                                              |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                  | Medienbild für WPD- \_ \_ Inhaltstyp \_ \_                                                                                                 |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                   |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                  | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                   |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                | Thur, 1. Juni 2006 14:00:28 (EDT)                                                                                                   |
| [WPD- \_ Objekt \_ Format](object-properties.md)                               | WPD- \_ Objekt \_ Format \_ MP3                                                                                                         |
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                       | Sitzungs abhängig. (Für dieses Beispiel wird "0a2" angenommen.)                                                                              |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                   | Die digitale Veröffentlichung                                                                                                          |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md) | Sitzungs unabhängig.                                                                                                             |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 




