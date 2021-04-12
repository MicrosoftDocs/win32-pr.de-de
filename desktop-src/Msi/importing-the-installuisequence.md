---
description: Die Benutzeroberflächen Sequenz wird in die-Beispieldatenbank importiert.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importieren der InstallUISequence-Sequenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216937"
---
# <a name="importing-the-installuisequence"></a>Importieren der InstallUISequence-Sequenz

In der [Tabelle InstallUISequence](installuisequence-table.md) sind Aktionen aufgeführt, die ausgeführt werden, wenn die [Installations Aktion](install-action.md) der obersten Ebene ausgeführt wird und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist. Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder auf keine Benutzeroberfläche festgelegt ist. Weitere Informationen finden Sie unter [Benutzeroberfläche](user-interface.md) und [Benutzeroberflächen Ebenen](user-interface-levels.md). Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden. Es sollten keine Änderungen an diesen Sequenzen notwendig sein, um das Notepad-Installationspaket zu erstellen.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle InstallUISequence ein.

[InstallUISequence-Tabelle](installuisequence-table.md)



| Aktion                | Bedingung                                    | Sequenz |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| Ccpsearch             | Nicht installiert                                | 500      |
| Costfinalize          |                                              | 1000     |
| Costinitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1300     |
| Exitdlg               |                                              | -1       |
| Fatalerrordlg         |                                              | -3       |
| Datei Kosten              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| Maintenancewelcomedlg | Installiert, nicht fortsetzen und nicht vorab ausgewählt | 1250     |
| Preparedlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| Resumedlg             | Installiert und (fortsetzen oder vorab ausgewählt)        | 1240     |
| RMCCPSEARCH           | Nicht installiert                                | 600      |
| Userexitdlg           |                                              | -2       |
| Welcomedlg            | Nicht installiert                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Fortsetzen](importing-the-adminexecutesequence.md)

 

 



