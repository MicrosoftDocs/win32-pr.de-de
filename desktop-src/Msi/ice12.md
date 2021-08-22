---
description: ICE12 überprüft die Tabellen CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence und InstallUISequence der Windows Installer-Datenbank.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef427ca1567680aa9a9f2a598f5a94cb8dee545487afcf3eb1fbb8d1f350fd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262260"
---
# <a name="ice12"></a>ICE12

ICE12 fragt die Tabellen [CustomAction,](customaction-table.md) [Directory,](directory-table.md) [AdminExecuteSequence,](adminexecutesequence-table.md) [AdminUISequence,](adminuisequence-table.md) [AdvtExecuteSequence,](advtexecutesequence-table.md) [InstallExecuteSequence](installexecutesequence-table.md)und [InstallUISequence](installuisequence-table.md) ab, um Folgendes zu überprüfen:

-   Die [Aktion CostFinalize](costfinalize-action.md) tritt in jeder Sequenztabelle auf, die Aktionen vom Typ Benutzerdefinierter Aktionstyp [35](custom-action-type-35.md) oder [Benutzerdefinierter Aktionstyp 51 enthält.](custom-action-type-51.md)
-   Dass jeder [benutzerdefinierte Aktionstyp 35](custom-action-type-35.md) nach der [CostFinalize-Aktion liegt.](costfinalize-action.md) in den Sequenztabellen.
-   Dass jeder [benutzerdefinierte Aktionstyp 51,](custom-action-type-51.md) der über einen Fremdschlüssel für die Directory-Tabelle in der Spalte Source der CustomAction-Tabelle verfügt, vor der [Aktion CostFinalize](costfinalize-action.md) in den Sequenztabellen steht.

Beachten Sie, dass ICE12 den formatierten Text in der Spalte Ziel der CustomAction-Tabelle nicht überprüft.

## <a name="result"></a>Ergebnis

ICE12 gibt eine Fehlermeldung aus, wenn die Validierung der benutzerdefinierten Aktionen, die eine Verzeichniseigenschaft festlegen, fehlschlägt.

## <a name="example"></a>Beispiel

ICE12 würde drei Fehler für das gezeigte Beispiel veröffentlichen.

-   Für CA1 wurde der Ordner "MyFolder" in der Verzeichnistabelle nicht gefunden.
-   Bei CA2 liegt die Sequenz "80" vor CostFinalize in der Tabelle InstallExecuteSequence. Er muss nach ( CF@100 ) kommen.
-   Bei CA3 folgt Sequenz "125" nach CostFinalize in der Tabelle InstallExecuteSequence. Er muss vor ( ) sein. CF@100

[CustomAction-Tabelle](customaction-table.md) (partiell)



| Aktion | type | `Source`        |
|--------|------|---------------|
| KA1    | 35   | Myfolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Verzeichnistabelle](directory-table.md)



| Verzeichnis     | Übergeordnetes Verzeichnis \_ | DefaultDir    |
|---------------|-------------------|---------------|
| Targetdir     |                   | SourceDir     |
| WindowsFolder | Targetdir         | WindowsFolder |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion       | Sequenz |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Um den Fehler für CA1 zu beheben, ändern Sie seinen Eintrag in der Quellspalte in der CustomAction-Tabelle in einen vorhandenen Eintrag in der Directory-Tabelle, oder fügen Sie MyFolder der Directory-Tabelle hinzu.

Um den Fehler für CA2 zu beheben, ändern Sie die Reihenfolge in der Tabelle InstallExecuteSequence so, dass sie nach der Aktion CostFinalize auftritt.

Um den Fehler für CA3 zu beheben, ändern Sie die Reihenfolge in der Tabelle InstallExecuteSequence so, dass sie vor der Aktion CostFinalize liegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



