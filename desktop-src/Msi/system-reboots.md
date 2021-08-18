---
description: Der Windows Installer kann ermitteln, wann ein Neustart des Systems erforderlich ist, und den Benutzer am Ende der Installation automatisch zum Neustart auffordern.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Systemneustarts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e5ff72b91b50a3da03fbfb0c52ff351af907c7f89b400120c463dab233f288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626830"
---
# <a name="system-reboots"></a>Systemneustarts

Der Windows Installer kann ermitteln, wann ein Neustart des Systems erforderlich ist, und den Benutzer am Ende der Installation automatisch zum Neustart auffordern. Beispielsweise fordert das Installationsprogramm automatisch zu einem Neustart auf, wenn dateien ersetzt werden müssen, die während der Installation verwendet werden.

Anwendungen, die [Windows Installer](windows-installer-portal.md) Version 4.0 oder höher für die Installation und Wartung verwenden, verwenden automatisch den [Neustart-Manager,](../rstmgr/restart-manager-portal.md) um Systemneustarts zu reduzieren. Windows Installationsprogrammversion 4.0 oder höher verfügt über Eigenschaften und Richtlinien, mit denen der Paketautor und die Administratoren die Interaktion des Windows Installers mit dem Neustart-Manager steuern können. Weitere Informationen finden Sie unter [Using Windows Installer with Restart Manager](using-windows-installer-with-restart-manager.md).

Autoren von Installationspaketen können Neustarts planen und unterdrücken, indem sie Standardaktionen in den Sequenztabellen verwenden und Eigenschaften festlegen. Die folgenden Aktionen und Eigenschaften werden verwendet, um Systemneustarts zu behandeln.



| Aktion, Dialogfeld oder Eigenschaft                                                | Kurzbeschreibung                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ForceReboot-Aktion](forcereboot-action.md)                                   | Fordert den Benutzer während der Installation zur Eingabe eines Neustarts auf.                                                                                                        |
| [ScheduleReboot-Aktion](schedulereboot-action.md)                             | Fordert den Benutzer am Ende der Installation zu einem Neustart auf.                                                                                                 |
| [**REBOOT-Eigenschaft**](reboot.md)                                              | Erzwingt oder unterdrückt bestimmte automatische Aufforderungen für einen Systemneustart.                                                                                           |
| [**REBOOTPROMPT-Eigenschaft**](rebootprompt.md)                                  | Unterdrückt die Anzeige von Aufforderungen für Neustarts für den Benutzer. Alle erforderlichen Neustarts werden automatisch ausgeführt.                                                           |
| [**AFTERREBOOT-Eigenschaft**](afterreboot.md)                                    | Wird häufig in einer Bedingung verwendet, die für die ForceReboot-Aktion erforderlich ist.                                                                                               |
| [InstallValidate-Aktion](installvalidate-action.md)                           | Zeigt bei Bedarf das Dialogfeld FilesInUse an, in dem Benutzer Prozesse herunterfahren und einige Systemneustarts vermeiden können.                              |
| [FilesInUse-Dialogfeld](filesinuse-dialog.md)                                     | Bietet Benutzern die Möglichkeit, Prozesse herunterfahren, um einige Systemneustarts zu vermeiden.                                                                              |
| [Dialogfeld "MsiRMFilesInUse"](msirmfilesinuse-dialog.md)                           | Bietet Benutzern die Möglichkeit, den [Neustart-Manager zum](../rstmgr/restart-manager-portal.md) Schließen und Neustarten von Anwendungen zu verwenden. Verfügbar ab Windows Installer-Version 4.0. |
| [**ReplacedInUseFiles-Eigenschaft**](replacedinusefiles.md)                      | Legen Sie fest, ob das Installationsprogramm über eine verwendete Datei installiert wird. Diese Eigenschaft wird von benutzerdefinierten Aktionen verwendet, um zu erkennen, dass ein Neustart erforderlich ist.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Eigenschaft zum Deaktivieren Windows Installer-Interaktion mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md). Verfügbar ab Windows Installer-Version 4.0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Gibt an, wie [der Neustart-Manager](../rstmgr/restart-manager-portal.md) Anwendungen schließt und neu startet. Verfügbar ab Windows Installer-Version 4.0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Gibt an, wie [der Neustart-Manager](../rstmgr/restart-manager-portal.md) Anwendungen schließt und neu startet. Verfügbar ab Windows Installer-Version 4.0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | Das Installationsprogramm legt diese Eigenschaft fest, wenn ein Neustart des Betriebssystems aussteht. Verfügbar ab Windows Installer-Version 4.0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Richtlinie zum Deaktivieren der Windows Installer-Interaktion mit [dem Neustart-Manager.](../rstmgr/restart-manager-portal.md) Verfügbar ab Windows Installer-Version 4.0.                |



 

FEHLER \_ INSTALL \_ SUSPEND bedeutet, dass die Installation nicht abgeschlossen wurde oder ein Rollback aufgetreten ist. Die Installation muss fortgesetzt werden, bevor sie abgeschlossen ist. Möglicherweise muss das System neu gestartet werden, bevor die Installation fortgesetzt werden kann.

Der Windows Installer gibt den Fehlercode ERROR \_ INSTALL \_ SUSPEND zurück, wenn die [ForceReboot-Aktion](forcereboot-action.md) ausgeführt wird. Er gibt ERROR SUCCESS REBOOT REQUIRED zurück, wenn vor dem Ausführen der Anwendung ein Neustart erforderlich ist, und gibt \_ \_ ERROR SUCCESS \_ \_ \_ REBOOT INITIATED zurück, \_ wenn das Installationsprogramm tatsächlich einen Neustart gestartet hat. Da Neustarts asynchron sind, kann der Neustart tatsächlich erfolgen, bevor der Fehlercode zurückgegeben wird. Weitere Informationen finden Sie unter [Fehlercodes](error-codes.md).

Benutzerdefinierte Aktionen können eine Aufforderung zum Neustart am Ende einer Installation erzwingen, indem Sie [**MsiSetMode aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) Benutzerdefinierte Aktionen können auch durch Aufrufen von MsiGetMode auf eine ausstehende [**Neustartaufforderung überprüfen.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)

## <a name="filesinuse-dialog"></a>FilesInUse-Dialogfeld

Das Installationsprogramm kann ermitteln, wann ein Neustart des Systems erforderlich ist, und den Benutzer zur Eingabe einer Anforderung zum Neustart auffordern. In der Regel ist ein Systemneustart erforderlich, da das Installationsprogramm versucht, eine Datei zu installieren, die derzeit verwendet wird. Wenn die [Aktion InstallValidate](installvalidate-action.md) die Installation einer Datei erkennt, die verwendet wird, wird das [Dialogfeld FilesInUse angezeigt.](filesinuse-dialog.md)

Wenn Sie davon ausgehen, dass das Installationsprogramm einen FilesInUseDialog-Befehl zeigt, dies jedoch nicht der Fall ist, kann dies aus einem der folgenden Gründe auftreten:

-   Die dateien, die verwendet werden, sind keine ausführbaren Dateien.
-   Das Installationsprogramm versucht nicht, diese Dateien zu installieren.
-   Der Prozess, der diese Dateien enthält, ist der Prozess, der die Installation aufruft.
-   Der Prozess, der diese Dateien enthält, ist ein Prozess, dem kein Fenster mit einem Titel zugeordnet ist.

Weitere Informationen finden Sie unter [Protokollierung von Neustartanforderungen.](logging-of-reboot-requests.md)

 

 
