---
description: Wenn dieses Bit festgelegt ist, werden die im Steuerelement aufgeführten Elemente in einer angegebenen Reihenfolge angezeigt. Wenn das-Bit nicht festgelegt ist, werden Elemente in alphabetischer Reihenfolge angezeigt.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Sortiertes Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041612"
---
# <a name="sorted-control-attribute"></a>Sortiertes Steuerelement Attribut

Wenn dieses Bit festgelegt ist, werden die im Steuerelement aufgeführten Elemente in einer angegebenen Reihenfolge angezeigt. Wenn das-Bit nicht festgelegt ist, werden Elemente in alphabetischer Reihenfolge angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[ListView-Steuerelement](listview-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **msidbcontrolattributess orted** |



 

## <a name="remarks"></a>Bemerkungen

Um die Elemente in einem Kombinations [Feld](combobox-control.md)zu sortieren, schließen Sie das sortierte Bit in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, und geben Sie die Element Reihenfolge in der Spalte Order der [ComboBox-Tabelle](combobox-table.md)an.

Um die Elemente in einem [ListBox](listbox-control.md)-Element zu sortieren, schließen Sie das sortierte Bit in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, und geben Sie die Element Reihenfolge in der Spalte Order der [ComboBox-Tabelle](combobox-table.md)an.

Wenn Sie die Elemente in einer [ListView](listview-control.md)sortieren möchten, schließen Sie das sortierte Bit in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, und geben Sie die Reihenfolge der Elemente in der [ComboBox-Tabelle](combobox-table.md)an.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



