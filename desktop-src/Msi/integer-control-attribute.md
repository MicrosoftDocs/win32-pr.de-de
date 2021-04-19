---
description: Wenn dieses Bit für ein Steuerelement festgelegt wird, ist die zugeordnete Eigenschaft, die in der Eigenschafts Spalte der Steuerelement Tabelle angegeben ist, eine ganze Zahl. Wenn dieses Bit nicht festgelegt ist, ist die Eigenschaft ein Zeichen folgen Wert.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Integer-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341179"
---
# <a name="integer-control-attribute"></a>Integer-Steuerelement Attribut

Wenn dieses Bit für ein Steuerelement festgelegt wird, ist die zugeordnete Eigenschaft, die in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md) angegeben ist, eine ganze Zahl. Wenn dieses Bit nicht festgelegt ist, ist die Eigenschaft ein Zeichen folgen Wert.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

[ComboBox](combobox-control.md)

[Bearbeiten](edit-control.md)

[ListBox](listbox-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 16      | 0x00000010  | **msidbcontrolattributesinteger** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das ganzzahlige Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



