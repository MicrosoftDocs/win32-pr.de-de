---
description: Wenn dieses Bit festgelegt ist, enthält radioButtonGroup Text und einen Rahmen, der um ihn herum angezeigt wird.
ms.assetid: 25f88e07-a17d-4a5a-bf4f-5615e371cf6b
title: HasBorder-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b67f642d6a3ab513c824633d981a99a1608b0f01b33b5f4b62adfd30550ca2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581380"
---
# <a name="hasborder-control-attribute"></a>HasBorder-Steuerelementattribut

Wenn dieses Bit festgelegt ist, enthält [radioButtonGroup](radiobuttongroup-control.md) Text und einen Rahmen, der um ihn herum angezeigt wird.

Wenn das Formatbit nicht festgelegt ist, wird der Rahmen nicht angezeigt, und in der Gruppe wird kein Text angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="valid"></a>Gültig



| Decimal  | Hexadezimal | Konstante                            |
|----------|-------------|-------------------------------------|
| 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festlegen zu können, schließen Sie die HasBorder-Bits in die Spalte Attribute des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere [Informationen finden Sie unter Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter Steuerelemente erstellen [müssen.](controls.md)

 

 



