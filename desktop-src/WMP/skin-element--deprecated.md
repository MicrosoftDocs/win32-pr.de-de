---
title: Skin-Element (veraltet)
description: Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Skin-Element (veraltet) Windows-Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355958"
---
# <a name="skin-element-deprecated"></a>Skin-Element (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Das **Skin** -Element gibt eine URL zu einem Rahmen an.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

URL für eine komprimierte Rahmen Datei mit der Dateinamenerweiterung. WMZ. Für Windows Media Player 9-Serie oder höher kann dieser Wert nur auf Border-Dateien auf der Festplatte des Benutzers verweisen, die sich im gleichen Verzeichnis wie die Metadatendatei-Wiedergabeliste befindet. Weitere Informationen finden Sie im Beispielcode.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente |
|-----------------|----------|
| Übergeordnete Elemente | **ASX**  |
| Untergeordnete Elemente  | Keine     |



 

## <a name="remarks"></a>Bemerkungen

Das **Skin** -Element wird zum Erstellen eines Rahmens verwendet, der mit einer Skin vergleichbar ist, aber im Bereich **jetzt Wiedergabe** der Windows-Media Player im Vollmodus angezeigt wird. Das **Skin** -Element wird nur für Rahmen verwendet, die innerhalb des Windows-Media Player im Vollmodus angezeigt werden, und nicht für reguläre Skins, die den Windows-Media Player im Compact-Modus vollständig ersetzen.

In einem Windows Media-Download Paket (mit der Dateinamenerweiterung ". WMD") ermöglicht das **Skin** -Element einem Rahmen, Inhalte zu erhalten und mit anderen Websites zu verknüpfen. Das Windows Media-Download Paket ist eine komprimierte Datei, die eine Rahmen Datei und eine Windows Media-Metadatendatei enthält. Die Rahmen Datei (mit der Dateinamenerweiterung. wmz) ist komprimiert und enthält eine Skin-Definitionsdatei (mit der Dateinamenerweiterung. WMS).

Ein **Skin** -Element hat drei Komponenten:

-   Ein Skin
-   Inhalt
-   Eine Metadatei

In Windows Media-Download Paketen enthaltene Skins müssen rechteckig in Form sein. Das Erstellen von Rahmen mit nicht rechteckigen Skins kann zu unerwarteten Ergebnissen führen.

## <a name="examples"></a>Beispiele


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rahmen für Windows-Media Player (veraltet)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





