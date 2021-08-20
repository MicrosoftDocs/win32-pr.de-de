---
description: ICE75 überprüft, ob alle benutzerdefinierten Aktionen vom Typ 17 (DLL), 18 (EXE), benutzerdefinierter Aktionstyp 21 (JScript) und benutzerdefinierter Aktionstyp 22 (VBScript) nach der Aktion CostFinalize sequenziert werden.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec625f3dd9d71daf8202423b6636d23db663aa15b9ab14c5362b63faf1df9e94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991055"
---
# <a name="ice75"></a>ICE75

ICE75 überprüft, ob alle benutzerdefinierten Aktionen vom Typ [17](custom-action-type-17.md) (DLL), [18](custom-action-type-18.md) (EXE), [benutzerdefinierter Aktionstyp 21](custom-action-type-21.md) (JScript) und [benutzerdefinierter Aktionstyp 22](custom-action-type-22.md) (VBScript) nach der [Aktion CostFinalize](costfinalize-action.md)sequenziert werden. Diese Arten von benutzerdefinierten Aktionen verwenden eine installierte Datei als Quelle. ICE75 überprüft die [Tabelle InstallUISequence,](installuisequence-table.md)die [Tabelle InstallExecuteSequence,](installexecutesequence-table.md)die [Tabelle AdminUISequence](adminuisequence-table.md)und die [Tabelle AdminExecuteSequence.](adminexecutesequence-table.md) Beachten Sie, dass die CostFinalize-Aktion in diesen Sequenztabellen erforderlich ist.

## <a name="result"></a>Ergebnis

ICE75 sendet einen Fehler, wenn eine benutzerdefinierte Aktion gefunden wird, die eine installierte Datei als Quelldatei verwendet, die nach der CostFinalize-Aktion nicht sequenziert wird.

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



| Aktion      | type | Quelle  |
|-------------|------|---------|
| CA \_ FileExe | 18   | FileExe |
| CA \_ FileDLL | 17   | FileDLL |



 

[AdminUISequence-Tabelle](adminuisequence-table.md) (partiell)



| Aktion      | Sequenz |
|-------------|----------|
| CA \_ FileExe | 1100     |



 

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md) (partiell)



| Aktion       | Sequenz |
|--------------|----------|
| CA \_ FileDLL  | 800      |
| CostFinalize | 1000     |



 

Sequenzieren Sie die benutzerdefinierten Aktionen nach der Aktion CostFinalize, um die Fehler zu beheben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



