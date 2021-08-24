---
description: Wenn dieses Formatbit festgelegt ist, wird der Text im -Steuerelement in einer Leserichtung von rechts nach links angezeigt.
ms.assetid: 68394498-98ca-4bcd-86c0-3f692a26a258
title: RTLRO-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c4488b31b0bac714d0f28915c074c0a6e4a8b5105e3ef2be60f3870ebcf88d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039670"
---
# <a name="rtlro-control-attribute"></a>RTLRO-Steuerelementattribut

Wenn dieses Formatbit festgelegt ist, wird der Text im -Steuerelement in einer Leserichtung von rechts nach links angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[GroupBox](groupbox-control.md)

 

[Progressbar](progressbar-control.md)

 

[Pushbutton](pushbutton-control.md)

 

[ScrollableText](scrollabletext-control.md)

 

[Text](text-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[CheckBox](checkbox-control.md)

 

[ComboBox](combobox-control.md)

 

[DirectoryList](directorylist-control.md)

 

[DirectoryCombo](directorycombo-control.md)

 

[Bearbeiten](edit-control.md)

 

[PathEdit](pathedit-control.md)

 

[ListBox](listbox-control.md)

 

[ListView](listview-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

 

[SelectionTree](selectiontree-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                        |
|---------|-------------|---------------------------------|
| 32      | 0x00000020  | **msidbControlAttributesRTLRO** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement zu festlegen, schließen Sie das RTLRO-Bit in die Spalte Attribute des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen [finden Sie unter Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



