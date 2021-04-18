---
description: Die Reboot-Eigenschaft unterdrückt bestimmte Aufforderungen für einen Neustart des Systems.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371599"
---
# <a name="reboot-property"></a>Reboot-Eigenschaft

Die **Reboot** -Eigenschaft unterdrückt bestimmte Aufforderungen für einen Neustart des Systems. Ein Administrator verwendet diese Eigenschaft in der Regel mit einer Reihe von Installationen, um mehrere Produkte gleichzeitig mit nur einem Neustart am Ende zu installieren. Weitere Informationen finden Sie unter [System Neustarts](system-reboots.md).

Die Aktionen [ForceReboot](forcereboot-action.md) und [schedulereboot](schedulereboot-action.md) informieren das Installationsprogramm darüber, dass der Benutzer aufgefordert wird, das System neu zu starten. Das Installationsprogramm kann auch feststellen, dass ein Neustart erforderlich ist, unabhängig davon, ob ForceReboot-oder schedulereboot-Aktionen in der Sequenz vorhanden sind. Beispielsweise fordert das Installationsprogramm automatisch einen Neustart an, wenn die während der Installation verwendeten Dateien ersetzt werden müssen.

Sie können bestimmte Eingabe Aufforderungen für Neustarts unterdrücken, indem Sie die Eigenschaft **Neustart** wie folgt festlegen.



| Neustart Wert   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Sie sollten am Ende der Installation immer zum Neustart aufgefordert werden. Die Benutzeroberfläche fordert den Benutzer immer auf, eine Option zum Neustart am Ende zu starten. Wenn keine Benutzeroberfläche vorhanden ist und es sich nicht um eine [Installation mit mehreren Paketen](multiple-package-installations.md)handelt, wird das System am Ende der Installation automatisch neu gestartet. Wenn es sich um eine Installation mit mehreren Paketen handelt, gibt es keinen automatischen Neustart des Systems, und das Installationsprogramm gibt einen Fehler bei \_ erfolgreicher \_ Neustarts \_ erforderlich zurück. |
| Suppress       | Unterdrücken von Eingabe Aufforderungen für einen Neustart am Ende der Installation. Das Installationsprogramm fordert den Benutzer nach wie vor auf, während der Installation neu zu starten, wenn die [ForceReboot-Aktion](forcereboot-action.md)auftritt. Wenn keine Benutzeroberfläche vorhanden ist, wird das System bei jedem ForceReboot automatisch neu gestartet. Neustarts am Ende der Installation (z. b. aufgrund des Versuchs, eine verwendete Datei zu installieren) werden unterdrückt.                                    |
| Unterdrücken von reallysup | Unterdrücken Sie alle Neustarts und Neustart Aufforderungen, die von ForceReboot während der Installation initiiert wurden. Unterdrücken Sie alle Neustarts, und starten Sie die Eingabe Aufforderungen am Ende der Installation. Die Neustart Aufforderung und der Neustart selbst werden unterdrückt. Beispielsweise wird am Ende der Installation ein Neustart durchgeführt, da der Versuch, eine verwendete Datei zu installieren, unterdrückt wird.                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Das Installationsprogramm wertet nur das erste Zeichen der **Reboot** -Eigenschaft aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**REBOOTPROMPT (Eigenschaft)**](rebootprompt.md)
</dt> <dt>

[System Neustarts](system-reboots.md)
</dt> </dl>

 

 




