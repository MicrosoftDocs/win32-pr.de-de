---
description: Wenn das Steuerelement "FixedSize" festgelegt ist, wird das Bild auf das Steuerelement zugeschnitten oder zentriert, ohne seine Form oder Größe zu ändern.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: FixedSize-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751144"
---
# <a name="fixedsize-control-attribute"></a>FixedSize-Steuerelement Attribut

Wenn das Steuerelement "FixedSize" festgelegt ist, wird das Bild auf das Steuerelement zugeschnitten oder zentriert, ohne seine Form oder Größe zu ändern.

Wenn dieses Bit nicht festgelegt ist, wird das Bild gestreckt, um es an das Steuerelement anzupassen.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Symbol:](icon-control.md)

[PUSHBUTTON](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                            |
|---------|-------------|-------------------------------------|
| 1048576 | 0x00100000  | **msidbcontrolattributesfixedsize** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das FixedSize-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Das Festlegen des FixedSize-Bits hat keine Auswirkung auf ein [CheckBox](checkbox-control.md), eine [pushtaste](pushbutton-control.md)oder eine [RadioButtonGroup](radiobuttongroup-control.md) , wenn weder die [Bitmap](bitmap-control-attribute.md) noch das [Symbol](icon-control-attribute.md) festgelegt wurde.

Wenn das FixedSize-Bit nicht festgelegt ist, hat dies keine Auswirkung auf ein Symbol Steuerelement oder ein einem Symbol [](iconsize-control-attribute.md) zugeordnetes PUSHBUTTON.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



