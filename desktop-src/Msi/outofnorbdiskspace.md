---
description: Das Installationsprogramm legt die OutOfNoRbDiskSpace-Eigenschaft auf True fest, wenn ein Volume, das ein Ziel der Installation ist, nicht über genügend Speicherplatz für die Installation verfügt.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: OutOfNoRbDiskSpace-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275eec4c78a1fe0074fe8e91f7dcab3b660cade46eb8810aa992edf6a45fb989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942770"
---
# <a name="outofnorbdiskspace-property"></a>OutOfNoRbDiskSpace-Eigenschaft

Das Installationsprogramm legt die **OutOfNoRbDiskSpace-Eigenschaft** auf True fest, wenn ein Volume, das ein Ziel der Installation ist, nicht über genügend Speicherplatz für die Installation verfügt. In diesem Fall wird die **OutOfNoRbDiskSpace-Eigenschaft** auf True festgelegt, auch wenn das Rollback deaktiviert wurde. Wenn alle Volumes über ausreichend Speicherplatz verfügen, ist der Wert False.

Ein Entwickler eines Installationspakets kann die Situation behandeln, in der die [**OutOfDiskSpace-Eigenschaft**](outofdiskspace.md) true und die **OutOfNoRbDiskSpace-Eigenschaft** false ist, indem er eine Benutzeroberfläche erstellt, die dem Benutzer die Möglichkeit bietet, das Rollback zu deaktivieren und die Installation fortzusetzen. Informationen zum bedingten Anzeigen eines Dialogfelds finden Sie unter [Übersicht über ControlEvent.](controlevent-overview.md) Informationen zum Deaktivieren des Rollbacks finden Sie unter [EnableRollback ControlEvent](enablerollback-controlevent.md).

Die **OutOfNoRbDiskSpace-Eigenschaft** ist jederzeit gültig, nachdem die [CostFinalize-Aktion](costfinalize-action.md) ausgeführt wurde. Der **OutOfNoRbDiskSpace-Eigenschaftsstatus** wird jedes Mal dynamisch aktualisiert, wenn die Gesamtinstallationskosten neu berechnet werden (z. B. jedes Mal, wenn der Installationsstatus eines Features über das [Dialogfeld Auswahl](selection-dialog.md)geändert wird). Auswahlauflösungsaktionen verwenden diesen Wert, um eine Installation abzubrechen und ein Dialogfeld zu generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Übersicht über ControlEvent](controlevent-overview.md)
</dt> <dt>

[**OutOfDiskSpace-Eigenschaft**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent](enablerollback-controlevent.md)
</dt> <dt>

[CostFinalize-Aktion](costfinalize-action.md)
</dt> <dt>

[Auswahldialogfeld](selection-dialog.md)
</dt> </dl>

 

 




