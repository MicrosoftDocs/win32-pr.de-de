---
title: Ambientattribute. clippingcolor
description: Das clippingcolor-Attribut gibt die Farbe an, die aus der clippingimage-Bitmap abgeschnitten werden soll, oder ruft diese ab.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- Ambientattribute. clippingcolor-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370748"
---
# <a name="ambientattributesclippingcolor"></a>Ambientattribute. clippingcolor

Das **clippingcolor** -Attribut gibt die Farbe an, die aus der **clippingimage** -Bitmap abgeschnitten werden soll, oder ruft diese ab.

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.



| Wert                                       | BESCHREIBUNG                                       |
|---------------------------------------------|---------------------------------------------------|
| Auto                                        | Standard. Die Farbe an Pixelposition 0, 0 wird verwendet. |
| Jeder Microsoft Internet Explorer-Farbwert | Die angegebene Internet Explorer-Farbe wird verwendet.    |



 

## <a name="remarks"></a>Bemerkungen

Die clippingfarbe gibt die Bereiche von **clippingimage** (oder **BackgroundImage** für **Ansicht** oder **unter Ansicht**) an, die transparenten, nicht klickbaren Teilen des Steuer Elements entsprechen. Die clippingfarbe kann angeben, dass mehrere Bereiche abgeschnitten werden sollen. Eine Warnung wird ausgegeben, wenn **clippingimage** ein JPG ist, um den Verlust von Farben in den JPGs zu warnen.

Das **clippingcolor** -Attribut wird vom **Wiedergabe** Listenelement nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. clippingimage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Farb Verweis**](color-reference.md)
</dt> </dl>

 

 





