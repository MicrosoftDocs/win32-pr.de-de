---
title: Ambientattribute. HorizontalAlignment
description: Mit dem HorizontalAlignment-Attribut wird ein Wert angegeben oder abgerufen, der die horizontale Platzierung des Steuer Elements angibt, wenn die Größe der Sicht oder der übergeordneten unter Ansicht geändert wird.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Ambientattribute. HorizontalAlignment-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359222"
---
# <a name="ambientattributeshorizontalalignment"></a>Ambientattribute. HorizontalAlignment

Mit dem **HorizontalAlignment** -Attribut wird ein Wert angegeben oder abgerufen, der die horizontale Platzierung des Steuer Elements angibt, wenn die Größe der **Sicht** oder der übergeordneten **unter Ansicht** geändert wird.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.



| Wert   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Linker Join    | Standard. Behält die Platzierung des-Steuer Elements relativ zur linken Seite der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                               |
| Rechts   | Behält die Platzierung des Steuer Elements relativ zur rechten Ecke der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                                       |
| Zentrum  | Behält die Platzierung des-Steuer Elements relativ zur horizontalen Mitte der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                           |
| strecken | Verwaltet die Platzierung des-Steuer Elements relativ zum linken und rechten Rand der **Sicht** oder übergeordneten **unter Ansicht** , wenn die Größe geändert wird. Das Steuerelement wird gestreckt, damit es passt, wenn die **Ansicht** oder die **unter Ansicht** gestreckt wird. Das tatsächliche Bild wird nicht vergrößert oder verkleinert, es sei denn, die Größe kann geändert werden, aber der durch Klicken aktivierbare Bereich wächst oder verkleinert, wenn er nicht von einem **clippingimage** festgelegt ist. |



 

## <a name="remarks"></a>Bemerkungen

Wenn " **HorizontalAlignment** " nicht auf "Center" festgelegt ist, behält das Steuerelement seinen ursprünglichen Abstand vom angegebenen Rand oder von beiden Kanten, wenn "Stretch" angegeben ist und die Größe des Steuer Elements geändert werden kann. Wenn das Steuerelement nicht in der Größe geändert werden kann und "Stretch" angegeben ist, wird stattdessen der durch Klicken aktivierbare Bereich gestreckt.

Sie können eine beliebige Kombination von **HorizontalAlignment** und **VerticalAlignment** festlegen. Wenn Sie z. b. ein Steuerelement sowohl horizontal als auch vertikal zentrieren möchten, legen Sie HorizontalAlignment = "Center" VerticalAlignment = "Center" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. VerticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**Ambientattribute. clippingimage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





