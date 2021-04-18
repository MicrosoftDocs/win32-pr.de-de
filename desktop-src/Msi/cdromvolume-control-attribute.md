---
description: Wenn das cdromvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation sowie alle CD-ROM-Volumes an.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Cdromvolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357519"
---
# <a name="cdromvolume-control-attribute"></a>Cdromvolume-Steuerelement Attribut

Wenn das cdromvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation sowie alle CD-ROM-Volumes an.

Wenn dieses Bit nicht festgelegt ist, zeigt das-Steuerelement alle Volumes in der aktuellen-Installation an.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Directoriycombo](directorycombo-control.md)

 

[Volumecostlist](volumecostlist-control.md)

 

[Volumeselectcombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                              |
|---------|-------------|---------------------------------------|
| 524288  | 0x00080000  | **msidbcontrolattributescdromvolume** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das cdromvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



