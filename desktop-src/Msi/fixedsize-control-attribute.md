---
description: Wenn das FixedSize Control-Bit festgelegt ist, wird das Bild im Steuerelement zugeschnitten oder zentriert, ohne seine Form oder Größe zu ändern.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: FixedSize-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40094001115dc6e196e66075abe7ace7c93c8e715818ad34235f80caf8306a06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649700"
---
# <a name="fixedsize-control-attribute"></a>FixedSize-Steuerelementattribut

Wenn das FixedSize Control-Bit festgelegt ist, wird das Bild im Steuerelement zugeschnitten oder zentriert, ohne seine Form oder Größe zu ändern.

Wenn dieses Bit nicht festgelegt ist, wird das Bild gestreckt, um es an das Steuerelement anzupassen.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Symbol:](icon-control.md)

[Pushbutton](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                            |
|---------|-------------|-------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das FixedSize-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Das Festlegen des FixedSize-Bits hat keine Auswirkungen auf [checkBox,](checkbox-control.md) [PushButton](pushbutton-control.md)oder [RadioButtonGroup,](radiobuttongroup-control.md) wenn weder die [Bitmap](bitmap-control-attribute.md) noch das [Symbol](icon-control-attribute.md) festgelegt wurden.

Das Festlegen des FixedSize-Bits hat keine Auswirkungen auf ein Symbolsteuerelement oder ein PushButton, das einem Symbol zugeordnet ist, wenn die [IconSize-Bits](iconsize-control-attribute.md) nicht festgelegt sind.

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



