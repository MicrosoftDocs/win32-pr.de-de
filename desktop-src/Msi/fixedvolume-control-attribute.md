---
description: Wenn das steuerungbit fixedvolume festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle festen internen Festplatten an.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Fixedvolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863551"
---
# <a name="fixedvolume-control-attribute"></a>Fixedvolume-Steuerelement Attribut

Wenn das steuerungbit fixedvolume festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle festen internen Festplatten an.

Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement die Volumes in der aktuellen Installation auf.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Directoriycombo](directorycombo-control.md)

 

[Volumecostlist](volumecostlist-control.md)

 

[Volumeselectcombo](volumeselectcombo-control.md)



| Decimal | Hexadezimal | Konstante                              |
|---------|-------------|---------------------------------------|
| 131072  | 0x00020000  | **msidbcontrolattributesfixedvolume** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das fixedvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



