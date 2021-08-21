---
description: Wenn das ComboList-Steuerelementbit für ein Kombinationsfeld festgelegt ist, wird das Bearbeitungsfeld durch ein statisches Textfeld ersetzt. Dadurch wird verhindert, dass ein Benutzer einen neuen Wert eingibt, und der Benutzer muss nur einen der vordefinierten Werte auswählen.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: ComboList-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e0a53357d91c5c5a016f65e8e1e0fb341b15cae1ea2c6cf480e536fa109067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145379"
---
# <a name="combolist-control-attribute"></a>ComboList-Steuerelementattribut

Wenn das ComboList-Steuerelementbit für ein Kombinationsfeld festgelegt ist, wird das Bearbeitungsfeld durch ein statisches Textfeld ersetzt. Dadurch wird verhindert, dass ein Benutzer einen neuen Wert eingibt, und der Benutzer muss nur einen der vordefinierten Werte auswählen.

Wenn dieses Bit nicht festgelegt ist, verfügt das Kombinationsfeld über ein Bearbeitungsfeld.

## <a name="valid-controls"></a>Gültige Steuerelemente

[ComboBox](combobox-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Beschreibung                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das ComboList-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



