---
description: Der Windows Installer kann ermitteln, wann ein Neustart des Systems erforderlich ist, und den Benutzer automatisch zum Neustart am Ende der Installation auffordern.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: System Neustarts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b32149bbcd43e284f45d7cabcba94a080be5262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356561"
---
# <a name="system-reboots"></a>System Neustarts

Der Windows Installer kann ermitteln, wann ein Neustart des Systems erforderlich ist, und den Benutzer automatisch zum Neustart am Ende der Installation auffordern. Der Installer fordert beispielsweise automatisch einen Neustart an, wenn er alle Dateien ersetzen muss, die während der Installation verwendet werden.

Anwendungen, die [Windows Installer](windows-installer-portal.md) Version 4,0 oder höher für die Installation und Wartung verwenden, verwenden automatisch den [Neustart-Manager](../rstmgr/restart-manager-portal.md) , um die Systemneustarts zu verringern. Windows Installer Version 4,0 oder höher verfügt über Eigenschaften und Richtlinien, mit denen der Paket Ersteller und Administratoren die Interaktion von Windows Installer mit dem Neustart-Manager steuern können. Weitere Informationen finden Sie unter [Verwenden von Windows Installer mit dem Neustart-Manager](using-windows-installer-with-restart-manager.md).

Autoren von Installationspaketen können Neustarts planen und unterdrücken, indem Sie Standard Aktionen in den Sequenz Tabellen verwenden und Eigenschaften festlegen. Die folgenden Aktionen und Eigenschaften werden verwendet, um Systemneustarts zu verarbeiten.



| Aktion, Dialogfeld oder Eigenschaft                                                | Kurzbeschreibung                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ForceReboot-Aktion](forcereboot-action.md)                                   | Fordert den Benutzer zur Eingabe eines Neustarts während der Installation auf.                                                                                                        |
| [Schedulereboot-Aktion](schedulereboot-action.md)                             | Fordert den Benutzer auf, am Ende der Installation einen Neustart auszuführen.                                                                                                 |
| [**Reboot-Eigenschaft**](reboot.md)                                              | Erzwingt oder unterdrückt bestimmte automatische Eingabe Aufforderungen für einen Systemneustart.                                                                                           |
| [**REBOOTPROMPT (Eigenschaft)**](rebootprompt.md)                                  | Unterdrückt die Anzeige von Eingabe Aufforderungen für Neustarts für den Benutzer. Alle benötigten Neustarts erfolgen automatisch.                                                           |
| [**Afterreboot (Eigenschaft)**](afterreboot.md)                                    | Wird häufig in einer Bedingung verwendet, die für die ForceReboot-Aktion durchgesetzt wird.                                                                                               |
| [InstallValidate-Aktion](installvalidate-action.md)                           | Zeigt ggf. das Dialog Feld FilesInUse an und bietet Benutzern die Möglichkeit, Prozesse zu beenden und einige Systemneustarts zu vermeiden.                              |
| [FilesInUse (Dialog Feld)](filesinuse-dialog.md)                                     | Bietet Benutzern die Möglichkeit, Prozesse zu beenden, um einige Systemneustarts zu vermeiden.                                                                              |
| [Dialog Feld "msirmfilesinuse"](msirmfilesinuse-dialog.md)                           | Gibt Benutzern die Möglichkeit, Anwendungen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) zu schließen und neu zu starten. Verfügbar ab Windows Installer Version 4,0. |
| [**Replacedinusefiles (Eigenschaft)**](replacedinusefiles.md)                      | Legen Sie fest, ob das Installationsprogramm über eine verwendete Datei installiert wird. Diese Eigenschaft wird von benutzerdefinierten Aktionen verwendet, um zu erkennen, dass ein Neustart erforderlich ist.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Eigenschaft zum deaktivieren Windows Installer Interaktion mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md). Verfügbar ab Windows Installer Version 4,0.          |
| [**Msidisablermrestart**](msidisablermrestart.md)                             | Gibt an, wie der [Neustart-Manager](../rstmgr/restart-manager-portal.md) Anwendungen schließt und neu startet. Verfügbar ab Windows Installer Version 4,0.                  |
| [**Msirmshutdown**](msirmshutdown.md)                                         | Gibt an, wie der [Neustart-Manager](../rstmgr/restart-manager-portal.md) Anwendungen schließt und neu startet. Verfügbar ab Windows Installer Version 4,0.                  |
| [**Msisystemrebootpending**](msisystemrebootpending.md)                       | Der Installer legt diese Eigenschaft fest, wenn ein Neustart des Betriebssystems aussteht. Verfügbar ab Windows Installer Version 4,0.                         |
| [Disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md) | Richtlinie zum deaktivieren Windows Installer Interaktion mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md). Verfügbar ab Windows Installer Version 4,0.                |



 

Fehler \_ beim Installieren von \_ Suspend bedeutet, dass die Installation nicht fertiggestellt oder zurückgesetzt wurde. Die Installation muss fortgesetzt werden, bevor Sie abgeschlossen ist. Möglicherweise muss das System neu gestartet werden, bevor die Installation fortgesetzt werden kann.

Der Windows Installer gibt den Fehlercode Fehler \_ beim Installieren von Suspend zurück, \_ Wenn die [ForceReboot-Aktion](forcereboot-action.md) ausgeführt wird. \_ \_ \_ Wenn ein Neustart erforderlich ist, bevor die Anwendung ausgeführt wird, wird ein Neustart des \_ Fehlers \_ "Fehler erfolgreich" zurückgegeben \_ . Beachten Sie Folgendes: da Neustarts asynchron sind, kann der Neustart tatsächlich erfolgen, bevor der Fehlercode zurückgegeben wird. Weitere Informationen finden Sie unter [Fehler Codes](error-codes.md).

Benutzerdefinierte Aktionen können eine Aufforderung zum Neustart am Ende einer Installation erzwingen, indem [**msisetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)aufgerufen wird. Benutzerdefinierte Aktionen können auch überprüfen, ob eine ausstehende Neustart Aufforderung angezeigt wird, indem Sie [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)aufrufen.

## <a name="filesinuse-dialog"></a>FilesInUse (Dialog Feld)

Das Installationsprogramm kann ermitteln, wann ein Neustart des Systems erforderlich ist, und den Benutzer zum Neustart auffordern. Häufig ist ein Systemneustart erforderlich, da das Installationsprogramm versucht, eine Datei zu installieren, die zurzeit verwendet wird. Wenn die [InstallValidate-Aktion](installvalidate-action.md) die Installation einer verwendeten Datei erkennt, wird das [Dialog Feld FilesInUse](filesinuse-dialog.md)angezeigt.

Wenn Sie davon ausgehen, dass das Installationsprogramm ein filesinusedialog anzeigt, dies jedoch nicht der Fall ist, kann dies auf einen der folgenden Gründe zurückzuführen sein:

-   Die verwendeten Dateien sind keine ausführbaren Dateien.
-   Der Installer versucht nicht, diese Dateien zu installieren.
-   Der Prozess, der diese Dateien enthält, ist der Prozess, der die Installation aufruft.
-   Der Prozess, der diese Dateien enthält, ist ein Fenster, dem kein Fenster mit einem Titel zugeordnet ist.

Weitere Informationen finden Sie unter [Protokollieren von Neustart Anforderungen](logging-of-reboot-requests.md).

 

 
