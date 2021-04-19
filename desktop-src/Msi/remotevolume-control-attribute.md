---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Remotevolumes an. Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Remotevolume-Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353046"
---
# <a name="remotevolume-control-attribute"></a>Remotevolume-Steuerungs Attribut

Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Remotevolumes an. Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Directoriycombo](directorycombo-control.md)

[Volumecostlist](volumecostlist-control.md)

[Volumeselectcombo](volumeselectcombo-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                               |
|---------|-------------|----------------------------------------|
| 262144  | 0x00040000  | **msidbcontrolattributesremotevolume** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das Remotevolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



