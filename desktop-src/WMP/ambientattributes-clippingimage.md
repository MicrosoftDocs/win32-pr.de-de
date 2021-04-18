---
title: Ambientattribute. clippingimage
description: Das clippingimage-Attribut gibt den Bereich an, an den das Steuerelement abgeschnitten wird, oder ruft ihn ab.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Ambientattribute. clippingimage-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365585"
---
# <a name="ambientattributesclippingimage"></a>Ambientattribute. clippingimage

Das **clippingimage** -Attribut gibt den Bereich an, an den das Steuerelement abgeschnitten wird, oder ruft ihn ab.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei angibt Er besitzt keinen Standardwert.

## <a name="remarks"></a>Bemerkungen

Das **clippingimage** -Attribut unterstützt PNG-, JPG-, BMP-und GIF-Dateien (ohne animierte GIFs). Da es sich bei den JPGs um Verlust Verluste handelt, werden Sie daher nicht für das Abschneiden von Images empfohlen.

Dieses Attribut ist nützlich, wenn Sie nur einen Teil des Steuerelement Bilds anzeigen möchten, nicht den gesamten rechteckigen Bereich. Das **clippingcolor** -Attribut gibt die Bereiche des clippingbilds an, die transparenten, nicht klickbaren Teilen des Steuer Elements entsprechen. Das Steuerelement kann daher eine beliebige Form aufweisen. Um optimale Ergebnisse zu erzielen, sollte das clippingbild die gleiche Größe wie das Steuerelement Bild aufweisen.

Das **clippingimage** -Attribut wird von den Elementen " **Wiedergabeliste**", " **View**" und " **subview** " nicht unterstützt. Ein clippingbild funktioniert nicht mit dem **Video** Element, wenn es sich um ein *Video* handelt. **Windows less** ist auf false festgelegt, ebenso wie das **Effects** -Element bei *Effekten*. " **Fenster** " ist auf "true" festgelegt.

Da die Verwendung von Clipping-Images zu Leistungseinbußen führt, sollten Sie nicht verwendet werden, wenn die Effizienz ein Problem ist.

## <a name="examples"></a>Beispiele

Ein Beispiel zur Veranschaulichung der Verwendung dieses Attributs finden Sie unter [ButtonElement. mappingColor](buttonelement-mappingcolor.md) -Attribut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. clippingcolor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





