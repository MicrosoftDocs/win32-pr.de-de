---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Wechsel Datenträger an. Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Removablevolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751128"
---
# <a name="removablevolume-control-attribute"></a>Removablevolume-Steuerelement Attribut

Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Wechsel Datenträger an. Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Directoriycombo](directorycombo-control.md)

 

[Volumecostlist](volumecostlist-control.md)

 

[Volumeselectcombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                  |
|---------|-------------|-------------------------------------------|
| 65536   | 0x00010000  | **msidbcontrolattributesremovablevolume** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das removablevolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



