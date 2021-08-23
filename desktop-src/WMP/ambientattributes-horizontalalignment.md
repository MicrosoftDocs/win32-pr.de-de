---
title: AmbientAttributes.horizontalAlignment
description: Das horizontalAlignment-Attribut gibt einen Wert an oder ruft einen Wert ab, der die horizontale Platzierung des Steuerelements angibt, wenn die Größe von VIEW oder der übergeordneten UNTERANSICHT geändert wird.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes.horizontalAlignment-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9daf64189735d79e1ad3eb4f7b3637ca68cfdae489cda9423bb60acdd1f9185c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055168"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes.horizontalAlignment

Das **horizontalAlignment-Attribut** gibt einen Wert an oder ruft einen Wert ab, der die horizontale Platzierung des Steuerelements angibt, wenn die Größe von **VIEW** oder der übergeordneten **UNTERANSICHT** geändert wird.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**



| Wert   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Linker Join    | Standard. Behält die Platzierung des Steuerelements relativ zur linken Seite der **VIEW-** oder übergeordneten **UNTERANSICHT** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                               |
| Rechts   | Behält die Platzierung des Steuerelements relativ zur rechten Seite von **VIEW** oder der übergeordneten **UNTERANSICHT** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                                       |
| Zentrum  | Behält die Platzierung des Steuerelements relativ zur horizontalen Mitte der **VIEW-** oder übergeordneten **UNTERANSICHT** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                           |
| strecken | Behält die Platzierung des Steuerelements relativ zum linken und rechten Rand der **VIEW-** oder übergeordneten **UNTERANSICHT** bei, wenn die Größe geändert wird. Das Steuerelement wird gestreckt, damit es passt, wenn **die VIEW-** **oder SUBVIEW-Ansicht** gestreckt wird. Das tatsächliche Bild wird nur dann größer oder verkleinert, wenn es in der Größe geändert werden kann, aber der klickbare Bereich wächst oder verkleinert sich, wenn er nicht durch ein **clippingImage-Objekt gebunden ist.** |



 

## <a name="remarks"></a>Hinweise

Sofern **horizontalAlignment** nicht auf "center" festgelegt ist, behält das Steuerelement seinen ursprünglichen Abstand vom angegebenen Rand oder von beiden Kanten bei, wenn "stretch" angegeben ist und die Größe des Steuerelements geändert werden kann. Wenn die Größe des Steuerelements nicht geändert werden kann und "stretch" angegeben ist, wird stattdessen der klickbare Bereich gestreckt.

Sie können eine beliebige Kombination aus **horizontalAlignment und** **verticalAlignment festlegen.** Wenn Sie beispielsweise ein Steuerelement horizontal und vertikal zentrieren möchten, legen Sie horizontalAlignment="center" verticalAlignment="center" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





