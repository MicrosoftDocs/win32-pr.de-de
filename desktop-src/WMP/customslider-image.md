---
title: Customslider. Image
description: Das Image-Attribut gibt den Namen der Datei an oder Ruft den Namen der Datei ab, die den verschiedenen Zuständen des benutzerdefinierten Schiebereglers entspricht.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Windows-Media Player "customslider. Image"
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352005"
---
# <a name="customsliderimage"></a>Customslider. Image

Das **Image** -Attribut gibt den Namen der Datei an oder Ruft den Namen der Datei ab, die den verschiedenen Zuständen des benutzerdefinierten Schiebereglers entspricht.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Das **Image** -Attribut ist erforderlich. Es gibt eine Bilddatei an, die aus mindestens einem untergeordneten Bild besteht, das entweder horizontal oder vertikal angeordnet ist und die verschiedenen Zustände des benutzerdefinierten Schiebereglers darstellt. Jedes untergeordnete Image muss die gleichen Dimensionen wie das **positionImage** aufweisen, oder der benutzerdefinierte Schieberegler funktioniert nicht ordnungsgemäß. Die Höhe oder Breite des gesamten Bilds muss daher ein gleich Vielfaches der Höhe oder Breite des **positionbilds** sein.

Die unterstützten Bild Dateitypen sind BMP, JPG, PNG und GIF (keine animierten GIFs).

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel für ein benutzerdefiniertes Schieberegler-Image. Das entsprechende **positionImage** wird im Beispiel Abschnitt der **positionImage** -Eigenschaft angezeigt.

![Beispiel eines customslider-Bilds](images/dial.png)

Das **positionImage** -Attribut enthält auch ein Codebeispiel, das veranschaulicht, wie die Attribute des **customslider** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Customslider-Element**](customslider-element.md)
</dt> <dt>

[**Customslider. positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





