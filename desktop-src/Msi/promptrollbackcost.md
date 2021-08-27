---
description: Die PROMPTROLLBACKCOST-Eigenschaft gibt die Aktion an, die das Installationsprogramm ausführen soll, wenn Rollbackinstallationsfunktionen aktiviert sind und nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen. Die möglichen Werte von PROMPTROLLBACKCOST lauten wie folgt. ValueActionPAnzeigen Sie ein Dialogfeld, in dem Sie gefragt werden, ob ohne Rollback fortzufahren ist. DDisable rollback and continue without asking user(DDisable rollback and continue without asking user) (DDisable rollback and continue without asking user(D FFail mit der Fehleraufforderung für nicht verfügbaren Speicherplatz.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: PROMPTROLLBACKCOST(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71cca3134593039354735e2e306a924620db8100eb0fd0e0a51f392c58f61897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129040"
---
# <a name="promptrollbackcost-property"></a>PROMPTROLLBACKCOST(Eigenschaft)

Die **PROMPTROLLBACKCOST-Eigenschaft** gibt die Aktion an, die das Installationsprogramm ausführen soll, wenn [Rollbackinstallationsfunktionen](rollback-installation.md) aktiviert sind und nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen.

Die möglichen Werte **von PROMPTROLLBACKCOST** lauten wie folgt.



| Wert | Aktion                                                              |
|-------|---------------------------------------------------------------------|
| P     | Zeigen Sie ein Dialogfeld an, in dem Sie gefragt werden, ob sie ohne Rollback fortgesetzt werden soll. |
| D     | Deaktivieren Sie das Rollback, und fahren Sie fort, ohne den Benutzer zu fragen.                  |
| F     | Fehler bei der Fehleraufforderung für nicht verfügbaren Speicherplatz.                       |



 

## <a name="remarks"></a>Hinweise

Wenn die Benutzeroberfläche auf der Benutzeroberflächenebene "Basic" oder "no" ausgeführt wird, verarbeitet das Installationsprogramm automatisch die logik für den speicherplatzbasierten Out-of-Disk-Bereich.

Wenn die Benutzeroberfläche auf der Ebene Vollständig ausgeführt wird, können dem Benutzer zusätzliche Optionen zur Verfügung stehen, z. B. die Eingabeaufforderung vor dem Fortsetzen eines Rollbacks, das Deaktivieren des Rollbacks oder das Fortsetzen ohne Rollback, wenn der Datenträger voll ist. Der Paketentwickler muss die Dialogfeldsequenz erstellen, um dem Benutzer die entsprechenden Optionen zur Verfügung zu stellen. Dazu stehen die [EnableRollback ControlEvent-Eigenschaft,](enablerollback-controlevent.md) [**die OutOfDiskSpace-Eigenschaft,**](outofdiskspace.md) die [**OutOfNoRbDiskSpace-Eigenschaft**](outofnorbdiskspace.md) und die **PROMPTROLLBACKCOST-Eigenschaft zur** Verfügung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




