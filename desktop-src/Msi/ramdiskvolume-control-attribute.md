---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle RAM-Datenträgervolumes an. Wenn dieses Bit nicht festgelegt ist, listet das -Steuerelement Volumes in der aktuellen Installation auf.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: RAMDiskVolume-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9167c045a8437fff12c312999d71bd8fc2c7927f1ac8d3acf2260127b73cbb83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129020"
---
# <a name="ramdiskvolume-control-attribute"></a>RAMDiskVolume-Steuerelementattribut

Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle RAM-Datenträgervolumes an. Wenn dieses Bit nicht festgelegt ist, listet das -Steuerelement Volumes in der aktuellen Installation auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Hinweise

Wenn Sie dieses Attribut für ein Steuerelement festlegen möchten, schließen Sie das RAMDiskVolume-Bit in die Spalte Attribute des Datensatzes des Steuerelements in der [Control-Tabelle ein.](control-table.md)

Weitere Informationen [finden Sie unter Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



