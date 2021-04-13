---
description: Wenn das floppyvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Disketten Volumes an.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Floppyvolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528184"
---
# <a name="floppyvolume-control-attribute"></a>Floppyvolume-Steuerelement Attribut

Wenn das floppyvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Disketten Volumes an.

Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Directoriycombo](directorycombo-control.md)

[Volumecostlist](volumecostlist-control.md)

[Volumeselectcombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                               |
|---------|-------------|----------------------------------------|
| 2097152 | 0x00200000  | **msidbcontrolattributesfloppyvolume** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das floppyvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



