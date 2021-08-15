---
title: LIDER.image
description: Das Imageattribut gibt den Namen der Datei an, die die Bilder enthält, die den verschiedenen Zustände des benutzerdefinierten Schiebereglers entspricht, oder ruft diesen ab.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- LIDER.image-Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b169bbdcac0e251a161c8e09f352caf460280b23e0198167a641721caa6c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936248"
---
# <a name="customsliderimage"></a>LIDER.image

Das  Imageattribut gibt den Namen der Datei an, die die Bilder enthält, die den verschiedenen Zustände des benutzerdefinierten Schiebereglers entspricht, oder ruft diesen ab.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Das  Imageattribut ist erforderlich. Sie gibt eine Bilddatei an, die aus einem oder mehreren untergeordneten Bildern besteht, die entweder horizontal oder vertikal angeordnet sind und die verschiedenen Zustände des benutzerdefinierten Schiebereglers darstellen. Jedes Unterbild muss die gleichen Dimensionen wie **das positionImage** haben, oder der benutzerdefinierte Schieberegler funktioniert nicht ordnungsgemäß. Die Höhe oder Breite des Gesamtbilds muss daher ein gleichmäßiges Vielfaches der Höhe oder Breite von **positionImage sein.**

Die unterstützten Bilddateitypen sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie ein Beispiel für ein benutzerdefiniertes Schiebereglerbild. Das entsprechende **positionImage** wird im Beispielabschnitt der **positionImage-Eigenschaft** angezeigt.

![Beispielbild eines Liders](images/dial.png)

Das **attribut positionImage** enthält auch ein Codebeispiel, das veranschaulicht, wie die Attribute des **ELEMENTS VERDRLIDER** verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LIDER-Element**](customslider-element.md)
</dt> <dt>

[**LIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





