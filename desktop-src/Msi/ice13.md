---
description: ICE13 überprüft, ob Dialoge in Sequenz Tabellen in den Tabellen "AdminUISequence" oder "InstallUISequence" angezeigt werden. Dialoge dürfen nicht in den Tabellen InstallExecuteSequence, AdminExecuteSequence oder AdvtExecuteSequence aufgeführt werden.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960040"
---
# <a name="ice13"></a>ICE13

ICE13 überprüft, ob Dialoge in Sequenz Tabellen in den Tabellen " [AdminUISequence](adminuisequence-table.md)" oder " [InstallUISequence](installuisequence-table.md) " angezeigt werden. Dialoge dürfen nicht in den Tabellen [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) aufgeführt werden.

## <a name="result"></a>Ergebnis

ICE13 gibt eine Fehlermeldung aus, wenn ein Dialogfeld in einer Execute Sequence-Tabelle angezeigt wird.

## <a name="example"></a>Beispiel

Im folgenden Beispiel gibt ICE13 eine Fehlermeldung aus, die besagt, dass "welcomedialog" nicht in der Tabelle "InstallExecuteSequence" aufgeführt werden kann.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion          |
|-----------------|
| InstallFinalize wurde |
| Costfinalize    |
| Welcomedialog   |



 

[InstallUISequence-Tabelle](installuisequence-table.md) (partiell)



| Aktion         |
|----------------|
| Costfinalize   |
| Costinitialize |
| Browgdialog   |



 

[Dialog Feld Tabelle](dialog-table.md) (teilweise)



| Dialog        |
|---------------|
| Browgdialog  |
| Welcomedialog |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



