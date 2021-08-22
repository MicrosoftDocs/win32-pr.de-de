---
description: Wenn das FloppyVolume Control-Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Diskettenvolumes an.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: FloppyVolume-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4639960fee79336048082c91088e19c1b360f857216f2cf0ad9ed07c64b52b8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947011"
---
# <a name="floppyvolume-control-attribute"></a>FloppyVolume-Steuerelementattribut

Wenn das FloppyVolume Control-Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Diskettenvolumes an.

Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                               |
|---------|-------------|----------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das FloppyVolume-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



