---
description: In der Tabelle AdminExecuteSequence werden Aktionen aufgeführt, die vom Installationsprogramm ausgeführt werden, wenn die Administratoraktion der obersten Ebene aufruft. Weitere Informationen finden Sie unter Gruppe "Installationsprozedurtabellen", Verwenden einer Sequenztabelle und ausführliches Beispiel für die Sequenztabelle.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importieren von AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de646049fed05f881b61c4b635af3bc9d2caed09512a1ec89853066b0ba99c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787380"
---
# <a name="importing-the-adminexecutesequence"></a>Importieren von AdminExecuteSequence

In [der Tabelle AdminExecuteSequence](adminexecutesequence-table.md) sind Aktionen aufgeführt, die vom Installationsprogramm ausgeführt werden, wenn die ADMINISTRATORaktion der obersten [Ebene aufruft.](admin-action.md) Weitere Informationen [finden Sie unter Installationsprozedurtabellengruppe](installation-procedure-tables-group.md), [Verwenden einer Sequenztabelle](using-a-sequence-table.md)und im [ausführlichen Beispiel für die Sequenztabelle.](sequence-table-detailed-example.md)

Wenn Sie [](importing-a-blank-database.md) im Abschnitt Importieren einer leeren Datenbank uisample.msi aus dem Windows Installer SDK verwendet haben, enthalten die Sequenztabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktionssequenzen, die [unter](using-a-sequence-table.md)Verwenden einer Sequenztabelle beschrieben werden. Es sollten keine Änderungen an diesen Sequenzen erforderlich sein, um das Editor beispielinstallationspaket zu erstellen.

Verwenden Sie Ihren Datenbank-Editor, um MNP2000.msi, und geben Sie die folgenden Daten in die Tabelle AdminExecuteSequence ein.

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)



| Aktion              | Bedingung | Sequenz |
|---------------------|-----------|----------|
| CostFinalize        |           | 1000     |
| CostInitialize      |           | 800      |
| FileCost            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1500     |
| InstallValidate     |           | 1400     |



 

[Fortsetzen](importing-the-adminuisequence.md)

 

 



