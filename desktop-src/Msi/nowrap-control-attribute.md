---
description: Wenn dieses Bit festgelegt ist, wird der Text im Steuerelement in einer einzelnen Zeile angezeigt. Wenn der Text über die Ränder des Steuerelements hinausgeht, wird er abgeschnitten und mit auslassungspunkten (&\# 0034;...&\# 0034;) wird am Ende eingefügt, um die Kürzung anzugeben. Wenn dieses Bit nicht festgelegt ist, wird text umbrochen.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ef67a58dd0898b4c1e6d1577d35d67e8810649d49425087fecc3e0b3518cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519640"
---
# <a name="nowrap-control-attribute"></a>NoWrap-Steuerelementattribut

Wenn dieses Bit festgelegt ist, wird der Text im Steuerelement in einer einzelnen Zeile angezeigt. Wenn der Text über die Ränder des Steuerelements hinausgeht, wird er abgeschnitten, und am Ende wird eine Auslassungszeichen ("...") eingefügt, um die Kürzung anzugeben. Wenn dieses Bit nicht festgelegt ist, wird text umbrochen.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Text](text-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das NoWrap-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



