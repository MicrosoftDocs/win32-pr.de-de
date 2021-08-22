---
title: SKIN-Element (veraltet)
description: Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von Windows Media Player und des Windows Media Player SDK möglicherweise nicht verfügbar ist.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- SKIN-Element (veraltet) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507910"
---
# <a name="skin-element-deprecated"></a>SKIN-Element (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von Windows Media Player und des Windows Media Player SDK möglicherweise nicht verfügbar ist.

Das **SKIN-Element** gibt eine URL zu einem Rahmen an.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attribute

**HREF** (erforderlich)

URL für eine komprimierte Rahmendatei mit der Dateinamenerweiterung .wmz. Für Windows Media Player Serie 9 oder höher kann dieser Wert nur auf Rahmendateien auf der Festplatte des Benutzers verweisen, die sich im gleichen Verzeichnis wie die Wiedergabeliste der Metadatei befinden. Sehen Sie sich den Beispielcode an.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente |
|-----------------|----------|
| Übergeordnete Elemente | **Asx**  |
| Untergeordnete Elemente  | Keine     |



 

## <a name="remarks"></a>Bemerkungen

Das **SKIN-Element** wird verwendet, um einen Rahmen zu erstellen, der einer Skin ähnelt, aber im Bereich **Jetzt wiedergegeben** des vollständigen Modus Windows Media Player angezeigt wird. Das **SKIN-Element** wird nur für Rahmen verwendet, die im vollständigen Modus Windows Media Player angezeigt werden, und nicht für reguläre Skins, die den kompakten Modus vollständig ersetzen Windows Media Player.

In einem Windows Mediendownloadpaket (mit der Dateinamenerweiterung .wmd) ermöglicht das **SKIN-Element** einem Rahmen, Inhalte und Links zu anderen Websites zu erhalten. Das Windows Mediendownloadpaket ist eine komprimierte Datei, die eine Rahmendatei und eine Windows Media-Metadatei enthält. Die Rahmendatei (mit der Dateinamenerweiterung ".wmz") ist komprimiert und enthält eine Skindefinitionsdatei (mit der Dateinamenerweiterung WMS).

Ein **SKIN-Element** umfasst drei Komponenten:

-   Eine Skin
-   Einige Inhalte
-   Eine Metadatei

Skins, die in Windows Mediendownloadpaketen enthalten sind, müssen rechteckig sein. Das Erstellen von Rahmen mit nicht rechteckigen Skins kann zu unerwarteten Ergebnissen führen.

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
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rahmen für Windows Media Player (veraltet)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





