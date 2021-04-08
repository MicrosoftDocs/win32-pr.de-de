---
description: Wenn das Bitmap-Steuerelement Bit festgelegt ist, wird der Text im-Steuerelement durch ein Bitmap-Bild ersetzt. Die Text-Spalte in der Steuerelement Tabelle ist ein Fremdschlüssel in die binäre Tabelle.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Bitmap-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864436"
---
# <a name="bitmap-control-attribute"></a>Bitmap-Steuerelement Attribut

Wenn das Bitmap-Steuerelement Bit festgelegt ist, wird der Text im-Steuerelement durch ein Bitmap-Bild ersetzt. Die Text-Spalte in der [Steuerelement Tabelle](control-table.md) ist ein Fremdschlüssel in die [binäre Tabelle](binary-table.md).

Wenn dieses Bit nicht festgelegt ist, wird der Text im-Steuerelement in der Text-Spalte der [Steuerelement Tabelle](control-table.md)angegeben.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

 

[PUSHBUTTON](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbcontrolattributesbitmap** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das Bitmap-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Die Text-Spalte in der Steuerelement Tabelle wird als Fremdschlüssel für die [binäre Tabelle](binary-table.md)verwendet. Daher kann das Steuerelement kein Symbolbild und keinen Text enthalten.

Legen Sie nicht sowohl das [Symbol](icon-control-attribute.md) als auch das Bitmap-Bit fest.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



