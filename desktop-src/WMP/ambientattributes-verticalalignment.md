---
title: Ambientattribute. VerticalAlignment
description: Mit dem VerticalAlignment-Attribut wird ein Wert angegeben oder abgerufen, der die vertikale Platzierung des-Steuer Elements angibt, wenn die Sicht oder die übergeordnete unter Ansicht gestreckt wird.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Ambientattribute. VerticalAlignment-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354758"
---
# <a name="ambientattributesverticalalignment"></a>Ambientattribute. VerticalAlignment

Mit dem **VerticalAlignment** -Attribut wird ein Wert angegeben oder abgerufen, der die vertikale Platzierung des-Steuer Elements angibt, wenn die **Sicht** oder die übergeordnete **unter Ansicht** gestreckt wird.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.



| Wert   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Standard. Behält die Platzierung des-Steuer Elements relativ zum oberen Rand der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                             |
| bottom  | Behält die Platzierung des-Steuer Elements relativ zum unteren Rand der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                   |
| Zentrum  | Behält die Platzierung des-Steuer Elements relativ zur vertikalen Mitte der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                          |
| strecken | Verwaltet die Platzierung des-Steuer Elements relativ zum oberen und unteren Rand der Ansicht, wenn die Größe geändert wird. Das Steuerelement wird gestreckt, damit es passt, wenn die **Ansicht** oder die übergeordnete **unter Ansicht** gestreckt wird. Das tatsächliche Bild wird nicht vergrößert oder verkleinert, es sei denn, die Größe kann geändert werden, aber der durch Klicken aktivierbare Bereich wächst oder verkleinert, wenn er nicht von einem **clippingimage** festgelegt ist. |



 

## <a name="remarks"></a>Bemerkungen

Wenn **VerticalAlignment** nicht auf "Center" festgelegt ist, behält das Steuerelement seinen ursprünglichen Abstand vom angegebenen Rand oder von beiden Kanten bei Angabe von "Stretch", und die Größe des Steuer Elements kann geändert werden. Wenn das Steuerelement nicht in der Größe geändert werden kann und "Stretch" angegeben ist, wird stattdessen der durch Klicken aktivierbare Bereich gestreckt.

Sie können eine beliebige Kombination der Attribute **HorizontalAlignment** und **VerticalAlignment** festlegen. Wenn Sie z. b. möchten, dass ein Steuerelement sowohl horizontal als auch vertikal zentriert wird, legen Sie **HorizontalAlignment** auf "Center" und **VerticalAlignment** auf "Center" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. HorizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





