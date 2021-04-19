---
description: Die Tabelle AdminUISequence listet Aktionen auf, die das Installationsprogramm aufruft, wenn es die Administrator Aktion der obersten Ebene ausführt und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importieren der AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349349"
---
# <a name="importing-the-adminuisequence"></a>Importieren der AdminUISequence

Die [Tabelle AdminUISequence](adminuisequence-table.md) listet Aktionen auf, die das Installationsprogramm aufruft, wenn es die [Administrator Aktion](admin-action.md) der obersten Ebene ausführt und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist. Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist. Weitere Informationen finden Sie unter [Benutzeroberfläche](user-interface.md) und [Benutzeroberflächen Ebenen](user-interface-levels.md). Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden. Um das Notepad-Beispiel zu installieren, sollten keine Änderungen an diesen Sequenzen erforderlich sein.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle AdminExecuteSequence ein.

[AdminUISequence-Tabelle](adminuisequence-table.md)



| Aktion          | Bedingung | Sequenz |
|-----------------|-----------|----------|
| Adminwelcomedlg |           | 1230     |
| Costfinalize    |           | 1000     |
| Costinitialize  |           | 800      |
| ExecuteAction   |           | 1300     |
| Exitdlg         |           | -1       |
| Fatalerrordlg   |           | -3       |
| Datei Kosten        |           | 900      |
| Preparedlg      |           | 140      |
| ProgressDlg     |           | 1280     |
| Userexitdlg     |           | -2       |



 

[Fortsetzen](importing-the-advtexecutesequence.md)

 

 



