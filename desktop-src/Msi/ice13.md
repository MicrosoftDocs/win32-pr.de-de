---
description: ICE13 überprüft, ob Dialoge in Sequenztabellen in den Tabellen AdminUISequence oder InstallUISequence angezeigt werden. Dialoge dürfen nicht in den Tabellen InstallExecuteSequence, AdminExecuteSequence oder AdvtExecuteSequence aufgeführt werden.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc11f8254c721d404a65e63fc897aa6e55bc61364c768b48f2d5aded4348d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946634"
---
# <a name="ice13"></a>ICE13

ICE13 überprüft, ob Dialoge in Sequenztabellen in den Tabellen [AdminUISequence](adminuisequence-table.md)oder [InstallUISequence](installuisequence-table.md) angezeigt werden. Dialoge dürfen nicht in den Tabellen [InstallExecuteSequence,](installexecutesequence-table.md) [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) aufgeführt werden.

## <a name="result"></a>Ergebnis

ICE13 sendet eine Fehlermeldung, wenn ein Dialogfeld in einer Ausführungssequenztabelle angezeigt wird.

## <a name="example"></a>Beispiel

Im folgenden Beispiel sendet ICE13 eine Fehlermeldung, die besagt, dass "WelcomeDialog" nicht in der Tabelle "InstallExecuteSequence" aufgeführt werden kann.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion          |
|-----------------|
| InstallFinalize |
| CostFinalize    |
| WelcomeDialog   |



 

[InstallUISequence-Tabelle](installuisequence-table.md) (partiell)



| Aktion         |
|----------------|
| CostFinalize   |
| CostInitialize |
| BrowseDialog   |



 

[Dialogtabelle](dialog-table.md) (partiell)



| Dialog        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



