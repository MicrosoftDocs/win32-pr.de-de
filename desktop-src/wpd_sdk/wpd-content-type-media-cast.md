---
description: MEDIENCAST DES \_ WPD-INHALTSTYPS \_ \_ \_
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d45c9bc1e8e41bae526f02102d341ef00fad435
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423460"
---
# <a name="wpd_content_type_media_cast"></a>MEDIENCAST DES \_ WPD-INHALTSTYPS \_ \_ \_

Ein Objekt, das seinen Typ als WPD CONTENT TYPE MEDIA CAST beschreibt, \_ \_ stellt eine Auflistung \_ \_ verwandter Inhalte dar.

Ein Mediacast-Objekt kann als Containerobjekt bezeichnet werden, das verwandte Inhalte gruppiert, ebenso wie eine Wiedergabeliste Musik gruppiert. Häufig wird ein Mediacast-Objekt verwendet, um Medieninhalte zu gruppieren, die online veröffentlicht wurden. Beispielsweise kann ein RSS-Kanal als Mediacast-Objekt dargestellt werden, dessen Objektverweise auf Inhaltsobjekte verweisen, die jedes Element im Kanal darstellen.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname             |  Erforderlich oder optional         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich.                                                             |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                             |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich.                                                             |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                             |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.               |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Dies ist optional.                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                             |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                             |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                     | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.            |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                               | Erforderlich, wenn das Objekt gelöscht werden kann.                                |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [WPD \_ MEDIA \_ COPYRIGHT](media-properties.md)                                                     | Dies ist optional.                                                             |
| [WPD \_ MEDIA \_ PARENTAL \_ RATING](media-properties.md)                                        | Dies ist optional.                                                             |
| [WPD \_ MEDIA \_ META \_ GENRE](media-properties.md)                                                  | Dies ist optional.                                                             |
| [\_ \_ WPD-MEDIENUNTERTITEL \_](media-properties.md)                                                    | Dies ist optional.                                                             |
| [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)                                              | Empfohlen.                                                          |
| [\_WPD-MEDIENTITEL \_](media-properties.md)                                                             | Empfohlen.                                                          |
| [\_WPD-MEDIENBESITZER \_](media-properties.md)                                                             | Empfohlen.                                                          |
| [\_ \_ WPD-MEDIENVERWALTUNGS-EDITOR \_](media-properties.md)                                        | Empfohlen.                                                          |
| [WPD \_ \_ MEDIALES](media-properties.md)                                                     | Empfohlen.                                                          |
| [\_ \_ WPD-MEDIENQUELL-URL \_](media-properties.md)                                                  | Empfohlen.                                                          |
| [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md)                                        | Empfohlen.                                                          |
| [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)                                                 | Dies ist optional.                                                             |
| [WPD \_ MEDIA \_ GENRE](media-properties.md)                                                             | Dies ist optional.                                                             |
| [\_ \_ \_ WPD-MEDIENOBJEKTLESEZEICHEN](media-properties.md)                                        | Empfohlen                                                           |
| [WPD \_ MEDIA \_ LAST \_ BUILD \_ DATE](media-properties.md)                                       | Empfohlen.                                                          |
| [WPD \_ MEDIA \_ TIME \_ TO \_ LIVE](media-properties.md)                                             | Dies ist optional.                                                             |
| [\_ \_ WPD-MEDIENUNTERBESCHREIBUNG \_](object-properties.md)                                                                 | Dies ist optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                               | Erforderlich oder optional | BESCHREIBUNG                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)      | Dies ist optional.            | Enthält die Mediacastdateidaten. Wenn dieser Mediacast beispielsweise einen RSS-Kanal darstellt, kann dies das RSS-Dokument sein. |
| [**\_WPD-RESSOURCENMINIATURANSICHT \_**](wpd-resource-thumbnail.md)  | Dies ist optional.            | Enthält die Miniaturansicht, die diesen Mediacast darstellt.                                                                         |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | Dies ist optional.            | Enthält die Grafik für diesen Mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Zuordnung von RSS-Elementen und Mediacast-Eigenschaften

Ein RSS-Kanal kann als Mediacast-Objekt dargestellt werden, dessen Verweise auf Inhaltsobjekte zeigen, die jedes Element in einem bestimmten Kanal darstellen.

Die Elemente in einem RSS-Feed verfügen über die folgende Hierarchie und Attribute.


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



In der folgenden Tabelle sind die Kanalelemente in einem RSS-Feed und die entsprechenden WPD \_ CONTENT \_ TYPE MEDIA \_ \_ CAST-Eigenschaften aufgeführt.



| Channel-Element | RSS-Feedanforderung | Entsprechende Mediacast-Eigenschaft      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| category            | Dies ist optional.                | [WPD \_ MEDIA \_ GENRE](media-properties.md)                       |
| cloud               | Nicht zutreffend          | Nicht zutreffend                                                                 |
| Copyright           | Dies ist optional.                | [\_WPD-MEDIEN \_ COPYRIGHT](media-properties.md)               |
| description         | Erforderlich.                | [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)           |
| Docs                | Nicht zutreffend          | Nicht zutreffend                                                                 |
| Generator           | Nicht zutreffend          | Nicht zutreffend                                                                 |
| language            | Nicht zutreffend          | Nicht zutreffend                                                                 |
| lastBuildDate       | Dies ist optional.                | [WPD \_ MEDIA \_ LAST \_ BUILD \_ DATE](media-properties.md) |
| link                | Erforderlich.                | [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md)  |
| managingEditor      | Dies ist optional.                | [\_ \_ WPD-MEDIENVERWALTUNGS-EDITOR \_](media-properties.md)  |
| Pubdate             | Dies ist optional.                | [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)        |
| rating              | Nicht zutreffend          | Nicht zutreffend                                                                 |
| skipDays            | Nicht zutreffend          | Nicht zutreffend                                                                 |
| skipHours           | Nicht zutreffend          | Nicht zutreffend                                                                 |
| Textinput           | Nicht zutreffend          | Nicht zutreffend                                                                 |
| title               | Erforderlich.                | [\_WPD-OBJEKTNAME \_](object-properties.md)                      |
| ttl                 | Dies ist optional.                | [WPD \_ MEDIA \_ TIME \_ TO \_ LIVE](media-properties.md)       |
| Webmaster           | Dies ist optional.                | [WPD \_ \_ MEDIALES](media-properties.md)               |



 

In der folgenden Tabelle sind die Bildelemente in einem RSS-Feed und die entsprechenden WPD \_ CONTENT \_ TYPE MEDIA \_ \_ CAST-Eigenschaften aufgeführt.



| Image-Element | RSS-Feedanforderung | Mediacast-Eigenschaft                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| description       | Dies ist optional.                | [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)          |
| height            | Dies ist optional.                | [\_WPD-MEDIENHÖHE \_](media-properties.md)                    |
| link              | Dies ist optional.                | [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md) |
| title             | Dies ist optional.                | [\_WPD-OBJEKTNAME \_](object-properties.md)                     |
| url               | Dies ist optional.                | [\_ \_ WPD-MEDIENQUELLEN-URL \_](media-properties.md)           |
| width             | Dies ist optional.                | [\_WPD-MEDIENBREITE \_](media-properties.md)                      |



 

In der folgenden Tabelle sind die Elementelemente in einem RSS-Feed und die entsprechenden WPD \_ CONTENT \_ TYPE MEDIA \_ \_ CAST-Eigenschaften aufgeführt.



| Item-Element | attribute | RSS-Feedanforderung | Mediacast-Eigenschaft  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| author           |               | Dies ist optional.                | [WPD \_ MEDIA \_ INTERPRET](media-properties.md)                    |
| category         |               | Dies ist optional.                | [WPD \_ MEDIA \_ GENRE](media-properties.md)                      |
|                  | Domäne        | Nicht zutreffend          | Nicht zutreffend                                                                |
| description      |               | Dies ist optional.                | [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)          |
| Gehäuse        |               | Dies ist optional.                |                                                                                |
|                  | url           | Erforderlich.                | [\_ \_ WPD-MEDIENQUELLEN-URL \_](media-properties.md)           |
|                  | length        | Erforderlich.                | [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                     |
|                  | Typ          | Erforderlich.                | (Der MIME-Typ sollte dem Inhaltstyp der Eigenschaft zugeordnet werden.)                 |
| guid             |               | Dies ist optional.                | [\_ \_ WPD-MEDIEN-GUID](media-properties.md)                        |
|                  | isPermaLink   | Nicht zutreffend          | Nicht zutreffend                                                                |
| link             |               | Dies ist optional.                | [\_ \_ WPD-MEDIENZIEL-URL \_](media-properties.md) |
| Pubdate          |               | Dies ist optional.                | [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)       |
| source           |               | Nicht zutreffend          | Nicht zutreffend                                                                |
| title            |               | Dies ist optional.                | [\_WPD-OBJEKTNAME \_](object-properties.md)                     |



 

Das folgende Beispiel zeigt einen vollständigen RSS-Feed für einen fiktiven Podcast, der vom CEO eines Veröffentlichungsunternehmens bereitgestellt wurde.


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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Zuordnen von RSS-Kanalelementen zu WPD-Eigenschaftswerten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Kanalelementen im vorherigen Beispiel bestimmten WPD-Eigenschaften zugeordnet werden.



| WPD-Eigenschaft | Wert |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [WPD \_ MEDIA \_ COPYRIGHT](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. Alle Rechte vorbehalten.                                        |
| [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)                        | Peter Bankov, CEO von Lucerne Publishing, untersucht die neuesten Trends in Onlineveröffentlichungen. |
| [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [WPD \_ MEDIA \_ GENRE](media-properties.md)                                    | Neuigkeiten                                                                                          |
| [WPD \_ MEDIA \_ LAST \_ BUILD \_ DATE](media-properties.md)              | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [\_ \_ WPD-MEDIENVERWALTUNGS-EDITOR \_](media-properties.md)               | someone@example.com                                                                           |
| [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)                     | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [WPD \_ MEDIA \_ TIME \_ TO \_ LIVE](media-properties.md)                    | 240                                                                                           |
| [\_WPD-MEDIENTITEL \_](media-properties.md)                                    | Die digitale Veröffentlichung                                                                       |
| [\_ \_ WPD-MEDIENQUELL-URL \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [WPD \_ \_ MEDIALES](media-properties.md)                            | someone@example.com                                                                           |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                  | MEDIENCAST DES \_ WPD-INHALTSTYPS \_ \_ \_                                                               |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                  | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                | Fr, 9. Juni 2006 14:00:28 EDT                                                                 |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                               | WPD \_ OBJECT \_ FORMAT \_ ABSTRACT \_ MEDIA \_ CAST                                                    |
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                       | Sitzungsabhängiger Wert.                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                   | Die digitale Veröffentlichung                                                                       |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)     | Die digitale Veröffentlichung                                                                       |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                        | MyPodcasts (ein fiktiver Podcast-Ordner auf dem Gerät). Gehen Sie für dieses Beispiel von "0A0" aus.        |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md) | Sitzungsunabhängiger Wert. (In diesem Beispiel wird "0A1" angenommen.)                                   |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                       | 0A2 für N Elemente<br/>                                                                   |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                   | 13,790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Zuordnen von RSS-Bildelementen zu WPD-Eigenschaftswerten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Bildelementen im vorherigen Beispiel bestimmten WPD-Eigenschaften zugeordnet werden.



| WPD-Eigenschaft               |                         Wert                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)                                                   | Lucerne Logo                                        |
| [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [\_WPD-MEDIENHÖHE \_](media-properties.md)                                                             | 300                                                 |
| [\_ \_ WPD-MEDIENQUELL-URL \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_WPD-MEDIENBREITE \_](media-properties.md)                                                               | 300                                                 |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                              | Lucerne Publishing                                  |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN GELÖSCHT \_ WERDEN](attributes.md)                               | VARIANT \_ TRUE                                       |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN GELESEN \_ WERDEN](attributes.md)                                   | VARIANT \_ TRUE                                       |
| [\_ \_ WPD-RESSOURCENATTRIBUTFORMAT \_](resource-attribute-properties.md)                     | \_ \_ WPD-OBJEKTFORMAT \_ GIF                            |
| [WPD \_ RESOURCE \_ ATTRIBUTE \_ OPTIMAL \_ READ \_ BUFFER \_ SIZE](attributes.md) | 1024                                                |
| [\_ \_ WPD-RESSOURCENATTRIBUT \_ \_ GESAMTGRÖßE](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Zuordnen von RSS-Elementelementen zu WPD-Eigenschaftswerten

In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS Item-Elementen im vorherigen Beispiel bestimmten WPD-Eigenschaften zuordnen.



| WPD-Eigenschaft  | Wert                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [\_WPD-MEDIENTITEL \_](media-properties.md)                                    | Die digitale Veröffentlichung                                                                                                          |
| [\_WPD-MEDIENDAUER \_](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD \_ MEDIA \_ INTERPRET](media-properties.md)                                  | Luzern                                                                                                                          |
| [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)                        | Onlineveröffentlichungen ändern sich schnell. Ein CEO eines Herausgebers untersucht die Trends der letzten 5 Jahre und deren Auswirkungen. |
| [\_ \_ WPD-MEDIENZIEL-URL \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [WPD \_ MEDIA \_ GENRE](media-properties.md)                                    | Neuigkeiten                                                                                                                             |
| [\_ \_ WPD-MEDIEN-GUID](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)                     | Ite, 1. Juni 2006, 14:00:28 EDT                                                                                                   |
| [\_ \_ WPD-MEDIENQUELLEN-URL \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)            | 0A1                                                                                                                              |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                  | MEDIENBILD DES \_ WPD-INHALTSTYPS \_ \_ \_                                                                                                 |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                | Do, 1. Juni 2006 14:00:28 EDT                                                                                                   |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                  | Do, 1. Juni 2006 14:00:28 EDT                                                                                                   |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                | Do, 1. Juni 2006 14:00:28 EDT                                                                                                   |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                               | \_WPD-OBJEKTFORMAT \_ \_ MP3                                                                                                         |
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                       | Sitzungsabhängig. (Nehmen Sie für dieses Beispiel "0A2" an.)                                                                              |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                   | Die digitale Veröffentlichung                                                                                                          |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                        | 0A0                                                                                                                              |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md) | Sitzungsunabhängig.                                                                                                             |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 




