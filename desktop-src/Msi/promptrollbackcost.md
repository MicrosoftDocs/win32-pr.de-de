---
description: Die promptrollbackcost-Eigenschaft gibt die Aktion an, die das Installationsprogramm durchführt, wenn Rollback-Installationsfunktionen aktiviert sind und nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen. Die möglichen Werte von promptrollbackcost lauten wie folgt. Valueaktionpdisplay ein Dialogfeld mit der Frage, ob der Vorgang ohne Rollback fortgesetzt werden soll. Ddeaktivieren Sie das Rollback, und fahren Sie fort, ohne den Benutzer Ffail mit der Fehlermeldung "nicht genügend Speicherplatz".
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Promptrollbackcost (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356074"
---
# <a name="promptrollbackcost-property"></a>Promptrollbackcost (Eigenschaft)

Die **promptrollbackcost** -Eigenschaft gibt die Aktion an, die das Installationsprogramm durchführt, wenn [Rollback-Installations](rollback-installation.md) Funktionen aktiviert sind und nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen.

Die möglichen Werte von **promptrollbackcost** lauten wie folgt.



| Wert | Aktion                                                              |
|-------|---------------------------------------------------------------------|
| P     | Zeigt ein Dialogfeld an, in dem Sie gefragt werden, ob ohne Rollback fortgefahren werden |
| D     | Deaktivieren Sie Rollback, und fahren Sie ohne Benutzer ab.                  |
| F     | Fehler bei der Eingabeaufforderung für nicht genügend Speicherplatz.                       |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Benutzeroberfläche auf der Ebene "Standard" oder "keine Benutzeroberfläche" ausgeführt wird, verarbeitet das Installationsprogramm automatisch die gesamte Logik für nicht genügend Speicherplatz.

Wenn die Benutzeroberfläche vollständig ausgeführt wird, können dem Benutzer zusätzliche Optionen zugewiesen werden, z. b. eine Eingabeaufforderung, bevor ein Rollback ausgeführt wird, ein Rollback deaktiviert wird oder der Vorgang ohne Rollback fortgesetzt wird, wenn der Datenträger voll ist. Der Paket Entwickler muss die Dialogfeld Sequenz verfassen, um dem Benutzer die entsprechenden Optionen bereitzustellen. Die Elemente, die hierfür verfügbar sind, sind die [enablerollback ControlEvent](enablerollback-controlevent.md)-, [**outo fdiskspace**](outofdiskspace.md) -Eigenschaft, [**ouesfnorbdiskspace**](outofnorbdiskspace.md) -Eigenschaft und die **promptrollbackcost** -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




