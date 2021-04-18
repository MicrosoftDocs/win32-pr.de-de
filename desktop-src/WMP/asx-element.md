---
title: ASX-Element
description: Das Element "ASX" definiert eine Datei als Metadatei.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Fenster Media Player des ASX-Elements
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358705"
---
# <a name="asx-element"></a>ASX-Element

Das Element " **ASX** " definiert eine Datei als Metadatei.

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>Attribute

`VERSION` (erforderlich)

Dezimalzahl, die die Versionsnummer der Syntax für die Metadatei darstellt. Legen Sie auf 3 oder 3,0 fest.

**PreviewMode** (optional)

Ein Wert, der angibt, ob Windows Media Player vor dem ersten Clip in den Vorschaumodus wechselt.

Muss einen der folgenden Werte aufweisen.



| Wert | BESCHREIBUNG                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Windows Media Player wechselt in den Vorschaumodus, bevor der erste Clip wiedergegeben wird.                            |
| Nein    | Der Standardwert. Windows Media Player wird vor der Wiedergabe des ersten Clips nicht in den Vorschaumodus wechselt. |



 

**Bannerbar** (optional)

Ein Wert, der angibt, ob Windows Media Player Platz für eine Banner Grafik reserviert.

Muss einen der folgenden Werte aufweisen.



| Wert | BESCHREIBUNG                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Der Standardwert. Windows Media Player reserviert Speicherplatz für die Banner Leiste nur dann, wenn ein Inhalts Element eine enthält.                       |
| FIXED | Windows Media Player reserviert eine Banner Grafik für jeden wiedergegebenen Inhalt, unabhängig davon, ob es ein zugeordnetes Banner gibt. |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente | Keine. Das Element " **ASX** " muss das erste Element in jeder Metadatendatei sein.                                                                                                 |
| Untergeordnete Elemente  | **abstract**, **Author**, **Banner**, **Base**, **Copyright**, **Entry**, **ENTRYREF**, **Event**, **moreinfo**, **previewduration**, **param**, **Repeat**, **Title** |



 

## <a name="remarks"></a>Bemerkungen

Die ersten vier Zeichen einer Metadatei-Wiedergabeliste müssen "<ASX" lauten. Andere Elemente, die innerhalb des Gültigkeits Bereichs des **ASX** -Elements definiert sind, z. b. **Titel** und **Autor**, werden mit den von Windows Media Player angezeigten Informationen verknüpft.

Für Windows Media Player lautet die Syntax Versionsnummer 3,0. Windows Media Player unterstützt alle früheren Versionen der metadateisyntax. Zulässige Werte für das **Versions** Attribut sind 3,0 und 3 (ohne Dezimaltrennzeichen).

Wenn der Wert des **PreviewMode** -Attributs "yes" lautet, wechselt Windows Media Player sofort in den Vorschaumodus, bevor der erste Clip wiedergegeben wird. Wenn Windows Media Player in den Vorschaumodus wechselt, werden alle Clips in der Metadatei als Vorschau angezeigt. Das **previewduration** -Element bestimmt die Dauer jeder Vorschau.

Das Attribut " **bannerbar** " definiert, ob Windows Media Player Platz für eine Banner Grafik reserviert. Ein Banner ist eine Grafik, die im Videoanzeige Bereich angezeigt wird, während Medieninhalte abgespielt werden. (Verwenden Sie das **Banner** -Element, um dem Inhalt ein Banner hinzuzufügen.) Wenn der Wert von " **bannerbar** " "Fixed" ist, reserviert Windows Media Player Bannerbereich für jedes Medien Inhalts Objekt, ob der Medieninhalt über ein Banner verfügt. Wenn einem Medieninhalt kein Banner zugeordnet ist, ist der reservierte Speicherplatz schwarz. Wenn der Wert des **bannerbar** -Attributs "Auto" ist, reserviert Windows Media Player Platz für das Banner nur dann, wenn der Medieninhalt eine enthält.

Wenn Sie eine Metadatei mit mehreren Clips (**Entry** -oder **ENTRYREF** -Elemente) erstellen und den Wert des Attributs " **bannerbar** " auf "Auto" festlegen, wird die Größe von Windows Media Player ggf. geändert, um Platz für eine Banner Grafik für einen Clip zuzulassen. Anschließend wird die Größe wieder geändert, wenn der nächste Clip keine Banner Grafik enthält. Wenn die Größe des Fensters unverändert bleiben soll (es sei denn, die Videogröße wird geändert), verwenden Sie den Fixed-Wert für das **bannerbar** -Attribut.

Der für eine Banner Grafik reservierte Raum ist 32 Pixel hoch und 194 Pixel breit. Der reservierte Speicherplatz wird unter jedem gerenderten Videoinhalt und 6 Pixel oberhalb des unteren Randes des Videobereichs angezeigt. Dadurch wird Platz für den 6-Pixel-Videobereichs Rahmen ermöglicht. Der reservierte Bannerbereich wird horizontal zentriert.

Windows Media Player rendert die Grafik ab dem äußersten linken Pixel des Banner Raums. Wenn die Grafik den gesamten Bereich füllt, wird Sie horizontal zentriert angezeigt. Andernfalls werden nachfolgende Leerzeichen angezeigt. Beachten Sie, dass die minimale Breite von Windows-Media Player immer breiter als die Größe des Videoclips ist, unabhängig vom Wert des **bannerbar** -Attributs.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





