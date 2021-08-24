---
description: Die Benutzeroberflächensequenz wird in die Beispieldatenbank importiert.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importieren der InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c559f9c4ad2cbd766447d27c879246f0fbf6af1ff78e1e02dece17b362ad2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580660"
---
# <a name="importing-the-installuisequence"></a>Importieren der InstallUISequence

In [der Tabelle InstallUISequence](installuisequence-table.md) werden Aktionen aufgeführt, die ausgeführt werden, wenn die [INSTALL-Aktion](install-action.md) der obersten Ebene ausgeführt wird und die interne Benutzeroberflächenebene auf vollständige benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist. Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächenebene auf einfache Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist. Siehe [Benutzeroberfläche](user-interface.md) und [Benutzeroberfläche Ebenen](user-interface-levels.md). Weitere Informationen [finden Sie unter Installationsprozedurtabellengruppe](installation-procedure-tables-group.md), [Verwenden einer Sequenztabelle](using-a-sequence-table.md)und im [ausführlichen Beispiel für die Sequenztabelle.](sequence-table-detailed-example.md)

Wenn Sie [](importing-a-blank-database.md) im Abschnitt Importieren einer leeren Datenbank uisample.msi aus dem Windows Installer SDK verwendet haben, enthalten die Sequenztabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktionssequenzen, die [unter](using-a-sequence-table.md)Verwenden einer Sequenztabelle beschrieben werden. Es sollten keine Änderungen an diesen Sequenzen erforderlich sein, um das Editor zu erstellen.

Verwenden Sie ihren Datenbank-Editor, um MNP2000.msi, und geben Sie die folgenden Daten in die Tabelle InstallUISequence ein.

[InstallUISequence-Tabelle](installuisequence-table.md)



| Aktion                | Bedingung                                    | Sequenz |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| CCPSearch             | NICHT installiert                                | 500      |
| CostFinalize          |                                              | 1000     |
| CostInitialize        |                                              | 800      |
| Executeaction         |                                              | 1300     |
| ExitDlg               |                                              | –1       |
| FatalErrorDlg         |                                              | -3       |
| FileCost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | Installiert UND NICHT FORTSETZEN UND NICHT vorab ausgewählt | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | INSTALLIERT UND (RESUME ODER vorab ausgewählt)        | 1240     |
| RMCCPSearch           | NICHT installiert                                | 600      |
| UserExitDlg           |                                              | –2       |
| WelcomeDlg            | NICHT installiert                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Fortsetzen](importing-the-adminexecutesequence.md)

 

 



