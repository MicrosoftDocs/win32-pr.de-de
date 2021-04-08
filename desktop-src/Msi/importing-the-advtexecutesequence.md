---
description: In der AdvtExecuteSequence-Tabelle sind Aktionen aufgeführt, die vom Installer beim Ausführen der Ankündigungs Aktion der obersten Ebene aufgerufen werden. Weitere Informationen finden Sie in der Gruppe "Installationsprozedur Tabellen" unter Verwendung einer Sequenz Tabelle und im detaillierten Beispiel der Sequenz Tabelle.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importieren von AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757818"
---
# <a name="importing-the-advtexecutesequence"></a>Importieren von AdvtExecuteSequence

In der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) sind Aktionen aufgeführt, die vom Installer beim Ausführen der Ankündigungs [Aktion](advertise-action.md)der obersten Ebene aufgerufen werden. Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden. Es sollten keine Änderungen an diesen Sequenzen notwendig sein, um das Notepad-Beispiel Installationspaket zu erstellen.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)ein.

[AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)



| Aktion                | Bedingung | Sequenz |
|-----------------------|-----------|----------|
| Costfinalize          |           | 1000     |
| Costinitialize        |           | 800      |
| "Kreateshortcuts"       |           | 4500     |
| InstallFinalize wurde       |           | 6600     |
| Installinitialisieren     |           | 1500     |
| InstallValidate       |           | 1400     |
| PublishComponents     |           | 6200     |
| Publishfeatures       |           | 6300     |
| Publishproduct        |           | 6400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| Registermimeinfo      |           | 4900     |
| Registerprogidinfo    |           | 4800     |



 

Die [advtuisequence-Tabelle](advtuisequence-table.md) wird vom Installer nicht verwendet. Diese Tabelle sollte in der Installations Datenbank nicht vorhanden oder leer gelassen werden.

[Fortsetzen](adding-summary-information.md)

 

 



