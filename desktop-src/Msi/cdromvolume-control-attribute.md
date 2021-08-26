---
description: Wenn das C ENUMERATIONVolume Control-Bit festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation sowie alle CD-ROM-Volumes an.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: C ENUMERATIONVolume-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abd961ddfd710defea9b464ea861f731fcf84a0989062f0607fda8ced5b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078040"
---
# <a name="cdromvolume-control-attribute"></a>C ENUMERATIONVolume-Steuerelementattribut

Wenn das C ENUMERATIONVolume Control-Bit festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation sowie alle CD-ROM-Volumes an.

Wenn dieses Bit nicht festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation an.

## <a name="valid-controls"></a>Gültige Steuerelemente

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                              |
|---------|-------------|---------------------------------------|
| 524288  | 0x00080000  | **msidbControlAttributesC ENUMERATIONVolume** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das CREDOVolume-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



