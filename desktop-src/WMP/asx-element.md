---
title: ASX-Element
description: Das ASX-Element definiert eine Datei als Metadatei.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- ASX-Element Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 509cdbc25c57c6d0b556433c3bee8b1e68083248c8356769a31529b83c2df1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902829"
---
# <a name="asx-element"></a>ASX-Element

Das **ASX-Element** definiert eine Datei als Metadatei.

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

Dezimalzahl, die die Versionsnummer der Syntax für die Metadatei darstellt. Legen Sie auf 3 oder 3.0 fest.

**PREVIEWMODE** (optional)

Wert, der angibt, ob Windows Media Player in den Vorschaumodus wechselt, bevor der erste Clip wiedergegeben wird.

Dabei muss es sich um einen der folgenden Werte handeln.



| Wert | BESCHREIBUNG                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Windows Media Player wechselt in den Vorschaumodus, bevor der erste Clip wiedergegeben wird.                            |
| Nein    | Der Standardwert. Windows Media Player wechselt nicht in den Vorschaumodus, bevor der erste Clip wiedergegeben wird. |



 

**BANNERBAR** (optional)

Wert, der angibt, ob Windows Media Player Platz für eine Bannergrafik reserviert.

Dabei muss es sich um einen der folgenden Werte handeln.



| Wert | BESCHREIBUNG                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Der Standardwert. Windows Media Player reserviert nur Dann Speicherplatz für die Bannerleiste, wenn ein Inhaltsteil einen enthält.                       |
| FIXED | Windows Media Player reserviert einen festen Platz für eine Bannergrafik für jeden wiedergegebenen Inhalt, unabhängig davon, ob ein zugehöriges Banner vorhanden ist. |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente | Keine. Das **ASX-Element** muss das erste Element in jeder Metadatei sein.                                                                                                 |
| Untergeordnete Elemente  | **ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY** **, ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE** |



 

## <a name="remarks"></a>Hinweise

Die ersten vier Zeichen einer Metadateiwiedergabeliste müssen "<ASX" sein. Andere Elemente, die innerhalb des Bereichs des **ASX-Elements** definiert sind, z. B. **TITLE** und **AUTHOR,** werden den show-Informationen zugeordnet, die von Windows Media Player angezeigt werden.

Für Windows Media Player lautet die Syntaxversionsnummer 3.0. Windows Media Player unterstützt alle früheren Versionen der Metadateisyntax. Zulässige Werte für das **VERSION-Attribut** sind sowohl 3.0 als auch 3 (ohne Dezimaltrennzeichen).

Wenn der Wert des **PREVIEWMODE-Attributs** YES lautet, wechselt Windows Media Player sofort in den Vorschaumodus, bevor der erste Clip wiedergegeben wird. Wenn Windows Media Player in den Vorschaumodus wechselt, wird für jeden Clip, auf den in der Metadatei verwiesen wird, eine Vorschau angezeigt. Das **PREVIEWDURATION-Element** bestimmt die Dauer der einzelnen Vorschauversionen.

Das **BANNERBAR-Attribut** definiert, ob Windows Media Player Platz für eine Bannergrafik reserviert. Ein Banner ist eine Grafik, die während der Wiedergabe von Medieninhalten im Videoanzeigebereich angezeigt wird. (Verwenden  Sie das BANNER-Element, um dem Inhalt ein Banner hinzuzufügen.) Wenn der Wert von **BANNERBAR** auf FIXED festgelegt ist, reserviert Windows Media Player Bannerspeicherplatz für jeden Medieninhalt, unabhängig davon, ob der Medieninhalt über ein Banner verfügt. Wenn einem Medieninhalt kein Banner zugeordnet ist, ist der reservierte Speicherplatz schwarz. Wenn der Wert des **BANNERBAR-Attributs** AUTO ist, reserviert Windows Media Player nur Dann Speicherplatz für das Banner, wenn der Medieninhalt eines enthält.

Wenn Sie eine Metadatei mit mehreren Clips **(ENTRY-** oder **ENTRYREF-Elemente)** erstellen und den Wert des **BANNERBAR-Attributs** auf AUTO festlegen, kann Windows Media Player die Größe ändern, um Platz für eine Bannergrafik für einen Clip zuzulassen, und dann die Größe erneut ändern, wenn der nächste Clip keine Bannergrafik enthält. Wenn die Größe des Fensters gleich bleiben soll (außer wenn sich die Videogröße ändert), verwenden Sie den FIXED-Wert für das **BANNERBAR-Attribut.**

Der für eine Bannergrafik reservierte Platz ist 32 Pixel hoch und 194 Pixel breit. Der reservierte Speicherplatz wird unter allen gerenderten Videoinhalten und 6 Pixel über dem unteren Rand des Videobereichs angezeigt, sodass Platz für den Rahmen des 6-Pixel-Videobereichs vorhanden ist. Der reservierte Bannerbereich ist horizontal zentriert.

Windows Media Player rendert die Grafik beginnend im ganz linken Pixel des Bannerbereichs. Wenn die Grafik den gesamten Bereich ausfüllt, wird sie horizontal zentriert angezeigt. Andernfalls wird nachgestellter Speicherplatz vorhanden sein. Beachten Sie, dass die Mindestbreite von Windows Media Player immer breiter als die Größe des  Videoclips ist, unabhängig vom Wert des BANNERBAR-Attributs.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





