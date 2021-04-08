---
description: In der InstallExecuteSequence-Tabelle werden die Aktionen aufgelistet, die ausgeführt werden, wenn das Installationsprogramm die Installations Aktion der obersten Ebene ausführt. Weitere Informationen finden Sie in der Gruppe "Installationsprozedur Tabellen" unter Verwendung einer Sequenz Tabelle und im detaillierten Beispiel der Sequenz Tabelle.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importieren von InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e4728b0a59c92dcc0d007fc816fd298455e049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960155"
---
# <a name="importing-the-installexecutesequence"></a>Importieren von InstallExecuteSequence

In der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) werden die Aktionen aufgelistet, die ausgeführt werden, wenn das Installationsprogramm die [Installations Aktion](install-action.md)der obersten Ebene ausführt. Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden. Es sind keine Änderungen an diesen Sequenzen erforderlich, um das Notepad-Installationspaket zu erstellen.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle InstallExecuteSequence ein.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion                   | Bedingung     | Sequenz |
|--------------------------|---------------|----------|
| Zuordnung von "Zuweisung"    | Nicht installiert | 1550     |
| AppSearch                |               | 400      |
| BindImage                |               | 4300     |
| Ccpsearch                | Nicht installiert | 500      |
| Costfinalize             |               | 1000     |
| Costinitialize           |               | 800      |
| "Kreatefolders"            |               | 3700     |
| "Kreateshortcuts"          |               | 4500     |
| Delta Service Services           | VersionNT     | 2000     |
| Duplicatefiles           |               | 4210     |
| Datei Kosten                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize wurde          |               | 6600     |
| Installinitialisieren        |               | 1500     |
| Installodbc              |               | 5400     |
| Installdienste          | VersionNT     | 5800     |
| InstallValidate          |               | 1400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| "Muvefiles"                |               | 3800     |
| Patchdateien               |               | 4090     |
| ProcessComponents        |               | 1600     |
| PublishComponents        |               | 6200     |
| Publishfeatures          |               | 6300     |
| Publishproduct           |               | 6400     |
| RegisterClassInfo        |               | 4600     |
| Registercomplus          |               | 5.700     |
| RegisterExtensionInfo    |               | 4700     |
| Register Fonts            |               | 5300     |
| Registermimeinfo         |               | 4900     |
| Register Product          |               | 6100     |
| Registerprogidinfo       |               | 4800     |
| Registertypelibraries    |               | 5500     |
| Register User             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| Removeumgebfäden |               | 3300     |
| RemoveExistingProducts   |               | 6700     |
| RemoveFiles              |               | 3500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| Removeodbc               |               | 2400     |
| Removeregistryvalues     |               | 2600     |
| Removeshortcuts          |               | 3200     |
| RMCCPSEARCH              | Nicht installiert | 600      |
| SelfRegModules           |               | 5600     |
| Selfunregmodules         |               | 2200     |
| "Btodbcfolders"           |               | 1100     |
| Startdienste            | VersionNT     | 5900     |
| Stop Services             | VersionNT     | 1.900     |
| Unpublishcomponents      |               | 1.700     |
| Nicht publishfeatures        |               | 1800     |
| Unregisterclassinfo      |               | 2700     |
| Unregistercomplus        |               | 2100     |
| Unregisterextensioninfo  |               | 2800     |
| Unregisterfonts          |               | 2500     |
| Unregistermimeinfo       |               | 3000     |
| Unregisterprogidinfo     |               | 2900     |
| Unregistertypelibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| Write-Umgebungs Zeichenfolgen  |               | 5200     |
| "Write"-Werte           |               | 5100     |
| "Schreibegistryvalues"      |               | 5.000     |



 

[Fortsetzen](importing-the-installuisequence.md)

 

 



