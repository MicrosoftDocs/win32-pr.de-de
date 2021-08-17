---
description: In der Tabelle InstallExecuteSequence sind die Aktionen aufgeführt, die ausgeführt werden, wenn das Installationsprogramm die INSTALL-Aktion der obersten Ebene ausführt. Weitere Informationen finden Sie unter Tabellengruppe für Installationsprozedur, Verwenden einer Sequenztabelle und ausführliches Beispiel für die Sequenztabelle.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importieren von InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586557130c6aa9af197d5d28f6bd750f4de736feb6982f3b7f12ce73ccf41c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430770"
---
# <a name="importing-the-installexecutesequence"></a>Importieren von InstallExecuteSequence

Die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) listet die Aktionen auf, die ausgeführt werden, wenn das Installationsprogramm die [INSTALL-Aktion](install-action.md)der obersten Ebene ausführt. Weitere Informationen finden Sie unter [Installationsprozedurtabellengruppe](installation-procedure-tables-group.md), [Verwenden einer Sequenztabelle](using-a-sequence-table.md)und ausführliches Beispiel für [die Sequenztabelle.](sequence-table-detailed-example.md)

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) uisample.msi aus dem Windows Installer SDK verwendet haben, enthalten die Sequenztabellen in Ihrer Kopie von MNP2000.msi bereits die unter Verwenden einer [Sequenztabelle](using-a-sequence-table.md)beschriebenen vorgeschlagenen Aktionssequenzen. Zum Erstellen des Editor Installationspakets sind keine Änderungen an diesen Sequenzen erforderlich.

Verwenden Sie den Datenbank-Editor, um MNP2000.msi zu öffnen und die folgenden Daten in die Tabelle InstallExecuteSequence einzugeben.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion                   | Bedingung     | Sequenz |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | NICHT installiert | 1550     |
| AppSearch                |               | 400      |
| BindImage                |               | 4300     |
| CCPSearch                | NICHT installiert | 500      |
| CostFinalize             |               | 1000     |
| CostInitialize           |               | 800      |
| CreateFolders            |               | 3700     |
| CreateShortcuts          |               | 4500     |
| DeleteServices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| FileCost                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize          |               | 6600     |
| InstallInitialize        |               | 1500     |
| InstallODBC              |               | 5400     |
| InstallServices          | VersionNT     | 5800     |
| InstallValidate          |               | 1400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| MoveFiles                |               | 3800     |
| PatchFiles               |               | 4090     |
| ProcessComponents        |               | 1600     |
| PublishComponents        |               | 6200     |
| PublishFeatures          |               | 6300     |
| PublishProduct           |               | 6400     |
| RegisterClassInfo        |               | 4600     |
| RegisterComPlus          |               | 5.700     |
| RegisterExtensionInfo    |               | 4700     |
| RegisterFonts            |               | 5300     |
| RegisterMIMEInfo         |               | 4900     |
| RegisterProduct          |               | 6100     |
| RegisterProgIdInfo       |               | 4800     |
| RegisterTypeLibraries    |               | 5500     |
| RegisterUser             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| RemoveEnvironmentStrings |               | 3300     |
| RemoveExistingProducts   |               | 6700     |
| RemoveFiles              |               | 3500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| RemoveODBC               |               | 2400     |
| RemoveRegistryValues     |               | 2600     |
| RemoveShortcuts          |               | 3200     |
| RMCCPSearch              | NICHT installiert | 600      |
| SelfRegModules           |               | 5600     |
| SelfUnregModules         |               | 2200     |
| SetODBCFolders           |               | 1100     |
| StartServices            | VersionNT     | 5900     |
| StopServices             | VersionNT     | 1.900     |
| UnpublishComponents      |               | 1.700     |
| UnpublishFeatures        |               | 1800     |
| UnregisterClassInfo      |               | 2700     |
| Registrierung aufhebenComPlus        |               | 2100     |
| UnregisterExtensionInfo  |               | 2800     |
| UnregisterFonts          |               | 2500     |
| UnregisterMIMEInfo       |               | 3000     |
| UnregisterProgIdInfo     |               | 2900     |
| UnregisterTypeLibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| WriteEnvironmentStrings  |               | 5200     |
| WriteIniValues           |               | 5100     |
| WriteRegistryValues      |               | 5.000     |



 

[Fortsetzen](importing-the-installuisequence.md)

 

 



