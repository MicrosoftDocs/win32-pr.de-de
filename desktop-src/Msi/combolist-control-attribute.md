---
description: Wenn das combolist-Steuerelement Bit in einem Kombinations Feld festgelegt ist, wird das Bearbeitungsfeld durch ein statisches Textfeld ersetzt. Dadurch wird verhindert, dass ein Benutzer einen neuen Wert eingibt, und der Benutzer muss nur einen der vordefinierten Werte auswählen.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Combolist-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352430"
---
# <a name="combolist-control-attribute"></a>Combolist-Steuerelement Attribut

Wenn das combolist-Steuerelement Bit in einem Kombinations Feld festgelegt ist, wird das Bearbeitungsfeld durch ein statisches Textfeld ersetzt. Dadurch wird verhindert, dass ein Benutzer einen neuen Wert eingibt, und der Benutzer muss nur einen der vordefinierten Werte auswählen.

Wenn dieses Bit nicht festgelegt ist, weist das Kombinations Feld ein Bearbeitungsfeld auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[ComboBox](combobox-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | BESCHREIBUNG                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbcontrolattributescombolist |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das combolist-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



