---
description: ICE12 überprüft die Tabellen CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence und InstallUISequence der Windows Installer Datenbank.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368848"
---
# <a name="ice12"></a>ICE12

ICE12 fragt die Tabellen [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)und [InstallUISequence](installuisequence-table.md) ab, um Folgendes zu überprüfen:

-   Die [costfinalize-Aktion](costfinalize-action.md) findet in jeder Sequenz Tabelle statt, die Aktionen vom Typ [benutzerdefinierte Aktionstyp 35](custom-action-type-35.md) oder [benutzerdefinierter Aktionstyp 51](custom-action-type-51.md)enthält.
-   Jeder [benutzerdefinierte Aktionstyp 35](custom-action-type-35.md) kommt nach der [costfinalize-Aktion](costfinalize-action.md). in den Sequenz Tabellen.
-   Jeder [benutzerdefinierte Aktionstyp 51](custom-action-type-51.md) , der über einen Fremdschlüssel für die Verzeichnis Tabelle in der Quell Spalte der Tabelle "CustomAction" verfügt, kommt vor der [Aktion "costfinalize](costfinalize-action.md) " in den Sequenz Tabellen.

Beachten Sie, dass ICE12 den formatierten Text in der Ziel Spalte der Tabelle "CustomAction" nicht überprüft.

## <a name="result"></a>Ergebnis

ICE12 gibt eine Fehlermeldung aus, wenn die Validierung der benutzerdefinierten Aktionen, die eine Verzeichnis Eigenschaft festlegen, fehlschlägt.

## <a name="example"></a>Beispiel

ICE12 würde drei Fehler für das gezeigte Beispiel Posten.

-   Für CA1 wurde der Ordner "MyFolder" in der Verzeichnis Tabelle nicht gefunden.
-   Für "Ca2" kommt die Sequenz "80" vor "costfinalize" in der Tabelle "InstallExecuteSequence". Der Wert muss nach ( CF@100 ) liegen.
-   Für CA3 kommt die Sequenz "125" nach "costfinalize" in der Tabelle "InstallExecuteSequence". Er muss vor () stehen. CF@100

[CustomAction-Tabelle](customaction-table.md) (partiell)



| Aktion | type | `Source`        |
|--------|------|---------------|
| KA1    | 35   | MyFolder      |
| Ca2    | 35   | Verzeichnis Windows befinden |
| CA3    | 51   | Verzeichnis Windows befinden |



 

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis     | Über \_ geordnetes Verzeichnis | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| Verzeichnis Windows befinden | TARGETDIR         | Verzeichnis Windows befinden |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion       | Sequenz |
|--------------|----------|
| Costfinalize | 100      |
| Ca2          | 80       |
| CA3          | 125      |



 

Um den Fehler für CA1 zu beheben, ändern Sie den Eintrag in der Quell Spalte in der Tabelle CustomAction in einen vorhandenen Eintrag in der Verzeichnis Tabelle, oder fügen Sie der Verzeichnis Tabelle den Eintrag MyFolder hinzu.

Um den Fehler für "Ca2" zu beheben, ändern Sie die zugehörige Sequenz in der InstallExecuteSequence-Tabelle so, dass Sie nach der Aktion "costfinalize" angezeigt wird.

Um den Fehler für CA3 zu beheben, ändern Sie die zugehörige Reihenfolge in der InstallExecuteSequence-Tabelle so, dass Sie vor der costfinalize-Aktion steht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



