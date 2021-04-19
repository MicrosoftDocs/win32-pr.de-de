---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle RAM-Datenträgervolumes an. Wenn dieses Bit nicht festgelegt ist, werden vom Steuerelement Volumes in der aktuellen Installation aufgelistet.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Ramdiskvolume-Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363450"
---
# <a name="ramdiskvolume-control-attribute"></a>Ramdiskvolume-Steuerungs Attribut

Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle RAM-Datenträgervolumes an. Wenn dieses Bit nicht festgelegt ist, werden vom Steuerelement Volumes in der aktuellen Installation aufgelistet.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Directoriycombo](directorycombo-control.md)

 

[Volumecostlist](volumecostlist-control.md)

 

[Volumeselectcombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbcontrolattributesramdiskvolume** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das ramdiskvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



