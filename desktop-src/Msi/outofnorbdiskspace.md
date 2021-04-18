---
description: Der Installer legt die ouesfnorbdiskspace-Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Ouesbnorbdiskspace (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360933"
---
# <a name="outofnorbdiskspace-property"></a>Ouesbnorbdiskspace (Eigenschaft)

Der Installer legt die **ouesfnorbdiskspace** -Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen. In diesem Fall wird die **ouesfnorbdiskspace** -Eigenschaft auf true festgelegt, auch wenn das Rollback deaktiviert wurde. Wenn alle Volumes über genügend Speicherplatz verfügen, ist der Wert false.

Ein Entwickler eines Installationspakets kann die Situation behandeln, in der die [**outofdiskspace**](outofdiskspace.md) -Eigenschaft "true" ist, und die **outofnorbdiskspace** -Eigenschaft "false" ist, indem eine Benutzeroberfläche erstellt wird, die dem Benutzer die Möglichkeit gibt, das Rollback zu deaktivieren und die Installation fortzusetzen. Informationen zur bedingten Anzeige eines Dialog Felds finden Sie unter [ControlEvent Overview](controlevent-overview.md). Weitere Informationen zum Deaktivieren des Rollbacks finden Sie unter [enablerollback ControlEvent](enablerollback-controlevent.md).

Die **ouesfnorbdiskspace** -Eigenschaft ist jederzeit gültig, nachdem die [Aktion "costfinalize](costfinalize-action.md) " ausgeführt wurde. Der Status der **ouesfnorbdiskspace** -Eigenschaft wird bei jeder Neuberechnung der Gesamt Installationskosten dynamisch aktualisiert (z. b. wenn der Installationsstatus eines beliebigen Features über das [Auswahl Dialogfeld](selection-dialog.md)geändert wird). Auswahl Auflösungs Aktionen verwenden diesen Wert, um eine Installation abzubrechen und ein Dialogfeld zu generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[ControlEvent (Übersicht)](controlevent-overview.md)
</dt> <dt>

[**Ouesf Disk Space (Eigenschaft)**](outofdiskspace.md)
</dt> <dt>

[Enablerollback-ControlEvent](enablerollback-controlevent.md)
</dt> <dt>

[Costfinalize-Aktion](costfinalize-action.md)
</dt> <dt>

[Auswahl Dialogfeld](selection-dialog.md)
</dt> </dl>

 

 




