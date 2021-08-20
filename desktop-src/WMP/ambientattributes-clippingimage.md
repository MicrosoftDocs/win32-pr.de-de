---
title: AmbientAttributes.clippingImage
description: Das clippingImage-Attribut gibt den Bereich an oder ruft den Bereich ab, in dem das Steuerelement abgeschnitten werden soll.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes.clippingImage Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15302483143b17075b6a6164fcd05da80eb1c7c666a83c76a460408d70ac72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055188"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

Das **clippingImage-Attribut** gibt den Bereich an oder ruft den Bereich ab, in dem das Steuerelement abgeschnitten werden soll.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibzeichenfolge, die den Namen der Bilddatei angibt. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Das **clippingImage-Attribut** unterstützt PNG-, JPG-, BMP- und GIF-Dateien (ohne animierte GIFs). Da JPGs verlustbeendend sind und daher unerwarteten Farbwechseln unterliegen, werden sie für das Ausschneiden von Bildern nicht empfohlen.

Dieses Attribut ist nützlich, wenn Sie nur einen Teil des Steuerelementbilds und nicht den gesamten rechteckigen Bereich anzeigen möchten. Das **clippingColor-Attribut** gibt die Bereiche des Clippingbilds an, die transparenten, nicht klickbaren Teilen des Steuerelements entsprechen. Das Steuerelement kann daher eine beliebige Form haben. Um optimale Ergebnisse zu erzielen, sollte das Clippingbild die gleiche Größe wie das Steuerelementbild haben.

Das **clippingImage-Attribut** wird von den **PLAYLIST-,** **VIEW-** und **SUBVIEW-Elementen nicht** unterstützt. Ein Clippingbild funktioniert nicht mit dem **VIDEO-Element,** wenn *VIDEO*. **windowless ist** auf FALSE festgelegt, und mit dem **EFFECTS-Element,** wenn *EFFECTS*. **windowed** ist auf TRUE festgelegt.

Da die Verwendung von Clippingbildern leistungssentspricht, sollten sie nicht verwendet werden, wenn effizienz ein Problem ist.

## <a name="examples"></a>Beispiele

Im [ButtonELEMENT.mappingColor-Attribut](buttonelement-mappingcolor.md) finden Sie ein Beispiel, das die Verwendung dieses Attributs veranschaulicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





