---
description: ICE77 überprüft, ob benutzerdefinierte Aktionen mit dem Bitsatz "msidbcustomaction typeinscript" nach der InstallInitialize-Aktion und vor der InstallFinalize-Aktion sequenziert werden.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129972"
---
# <a name="ice77"></a>ICE77

ICE77 überprüft, ob benutzerdefinierte Aktionen mit dem Bitsatz " **msidbcustomaction typeinscript** " nach der [InstallInitialize-Aktion](installinitialize-action.md) und vor der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden. ICE77 überprüft die Sequenz in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) und der [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md).

## <a name="result"></a>Ergebnis

ICE77 gibt einen Fehler aus, wenn eine benutzerdefinierte in-Script-Aktion vor der InstallInitialize-Aktion oder nach der InstallFinalize-Aktion sequenziert wird.

ICE77 gibt einen Fehler aus, wenn die InstallInitialize-Aktion oder die InstallFinalize-Aktion fehlt.

## <a name="example"></a>Beispiel

ICE77 meldet die folgenden Fehler für das Beispiel:

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

[CustomAction-Tabelle](customaction-table.md) (partiell)



| Aktion              | type |
|---------------------|------|
| ZS \_ inscriptinstall | 1025 |
| ZS \_ inscriptadmin   | 1026 |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion              | Sequenz |
|---------------------|----------|
| ZS \_ inscriptinstall | 2000     |
| Installinitialisieren   | 1500     |



 

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md) (partiell)



| Aktion            | Sequenz |
|-------------------|----------|
| ZS \_ inscriptadmin | 1400     |
| Installinitialisieren | 1500     |
| InstallFinalize wurde   | 6600     |



 

Um die Fehler zu beheben, müssen Sie die benutzerdefinierten Aktionen in Skripts nach der InstallInitialize-Aktion und vor der InstallFinalize-Aktion sequenzieren. Die InstallInitialize-und InstallFinalize-Aktionen müssen in der InstallExecuteSequence-Tabelle und der AdminExecuteSequence-Tabelle vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



