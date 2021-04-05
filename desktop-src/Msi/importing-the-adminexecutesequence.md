---
description: Die Tabelle AdminExecuteSequence listet Aktionen auf, die vom Installationsprogramm ausgeführt werden, wenn es die Administrator Aktion der obersten Ebene aufruft. Weitere Informationen finden Sie in der Gruppe "Installationsprozedur Tabellen" unter Verwendung einer Sequenz Tabelle und im detaillierten Beispiel der Sequenz Tabelle.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importieren von "AdminExecuteSequence"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752784"
---
# <a name="importing-the-adminexecutesequence"></a>Importieren von "AdminExecuteSequence"

Die [Tabelle AdminExecuteSequence](adminexecutesequence-table.md) listet Aktionen auf, die vom Installationsprogramm ausgeführt werden, wenn es die [Administrator Aktion](admin-action.md)der obersten Ebene aufruft. Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden. Es sollten keine Änderungen an diesen Sequenzen notwendig sein, um das Notepad-Beispiel Installationspaket zu erstellen.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle AdminExecuteSequence ein.

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)



| Aktion              | Bedingung | Sequenz |
|---------------------|-----------|----------|
| Costfinalize        |           | 1000     |
| Costinitialize      |           | 800      |
| Datei Kosten            |           | 900      |
| Installadminpackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize wurde     |           | 6600     |
| Installinitialisieren   |           | 1500     |
| InstallValidate     |           | 1400     |



 

[Fortsetzen](importing-the-adminuisequence.md)

 

 



