---
description: ICE75 überprüft, ob alle benutzerdefinierten Aktions Typen 17 (dll), Custom Action Type 18 (exe), Custom Action Type 21 (JScript) und Custom Action Type 22 (VBScript) benutzerdefinierte Aktionen nach der costfinalize-Aktion sequenziert werden.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347358"
---
# <a name="ice75"></a>ICE75

ICE75 überprüft, ob alle benutzerdefinierten [Aktions Typen 17](custom-action-type-17.md) (dll), [Custom Action Type 18](custom-action-type-18.md) (exe), Custom [Action Type 21](custom-action-type-21.md) (JScript) und Custom [Action Type 22](custom-action-type-22.md) (VBScript) benutzerdefinierte Aktionen nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden. Diese Typen von benutzerdefinierten Aktionen verwenden eine installierte Datei als Quelle. ICE75 überprüft die Tabelle " [InstallUISequence](installuisequence-table.md)", " [InstallExecuteSequence Table](installexecutesequence-table.md)", " [AdminUISequence](adminuisequence-table.md)" und " [AdminExecuteSequence](adminexecutesequence-table.md)". Beachten Sie, dass die Aktion "costfinalize" in diesen Sequenz Tabellen erforderlich ist.

## <a name="result"></a>Ergebnis

ICE75 gibt einen Fehler aus, wenn eine benutzerdefinierte Aktion mithilfe einer installierten Datei als Quelldatei gefunden wird, die nach der costfinalize-Aktion nicht sequenziert wurde.

## <a name="example"></a>Beispiel

ICE75 meldet die folgenden Fehler für das gezeigte Beispiel:

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[CustomAction-Tabelle](customaction-table.md) (partiell)



| Aktion      | type | `Source`  |
|-------------|------|---------|
| \_Datei-exe-Datei | 18   | FileExe |
| ZS- \_ Datei-dll | 17   | Filedll |



 

[AdminUISequence-Tabelle](adminuisequence-table.md) (partiell)



| Aktion      | Sequenz |
|-------------|----------|
| \_Datei-exe-Datei | 1100     |



 

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md) (partiell)



| Aktion       | Sequenz |
|--------------|----------|
| ZS- \_ Datei-dll  | 800      |
| Costfinalize | 1000     |



 

Um die Fehler zu beheben, müssen Sie die benutzerdefinierten Aktionen nach der costfinalize-Aktion sequenzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



