---
title: AmbientAttributes.clippingColor
description: Das clippingColor-Attribut gibt die Farbe an, die aus der ClippingImage-Bitmap abgeschnitten werden soll, oder ruft sie ab.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes.clippingColor Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299ee63b93abfdea337bb25e8b399e6011fb42d7fa4e1e0c09b3feb259d4f1d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902810"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

Das **clippingColor-Attribut** gibt die Farbe an, die aus der **ClippingImage-Bitmap** abgeschnitten werden soll, oder ruft sie ab.

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**



| Wert                                       | BESCHREIBUNG                                       |
|---------------------------------------------|---------------------------------------------------|
| Automatisch                                        | Standard. Die Farbe an pixelposition 0,0 wird verwendet. |
| einen beliebigen Microsoft Internet Explorer-Farbwert | Die angegebene Internet Explorer wird verwendet.    |



 

## <a name="remarks"></a>Hinweise

Die Clippingfarbe gibt die Bereiche des **clippingImage** (oder **backgroundImage** für **VIEW** oder **SUBVIEW)** an, die transparenten, nicht klickbaren Teilen des Steuerelements entsprechen. Die Clippingfarbe kann mehrere Bereiche angeben, die abgeschnitten werden sollen. Eine Warnung wird ausgegeben, wenn **clippingImage ein** JPG ist, um vor Farbverlusten in JPGs zu warnen.

Das **clippingColor-Attribut** wird vom **PLAYLIST-Element nicht** unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Farbreferenz**](color-reference.md)
</dt> </dl>

 

 





