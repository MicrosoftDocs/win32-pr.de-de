---
description: Der Installer legt die ouesfdiskspace-Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der aktuellen Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Ouesf Disk Space (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364951"
---
# <a name="outofdiskspace-property"></a>Ouesf Disk Space (Eigenschaft)

Der Installer legt die **ouesfdiskspace** -Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der aktuellen Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen. Wenn alle Volumes über genügend Speicherplatz verfügen, ist der Wert false. Auswahl Auflösungs Aktionen verwenden diesen Wert, um eine Installation abzubrechen und ein Dialogfeld zu generieren.

Diese Eigenschaft ist jederzeit gültig, nachdem die [Aktion "costfinalize](costfinalize-action.md) " ausgeführt wurde. Der Status der [**ouesfnorbdiskspace**](outofnorbdiskspace.md) -Eigenschaft wird bei jeder Neuberechnung der Gesamt Installationskosten dynamisch aktualisiert (z. b. wenn der Installationsstatus eines beliebigen Features über das [Auswahl](selection-dialog.md) Dialogfeld geändert wird).

## <a name="remarks"></a>Bemerkungen

Alle Dialogfelder, die sich auf die **oudefdiskspace** -Eigenschaft stützen, um zu bestimmen, ob ein Dialogfeld angezeigt werden soll, müssen das Dialogfeld Format des Dialog Felds " [trackdiskspace](trackdiskspace-dialog-style-bit.md) " für das Dialogfeld festlegen, um den Speicherplatz

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




