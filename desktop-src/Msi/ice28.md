---
description: ICE28 wird häufig verwendet, um zu überprüfen, ob die ForceReboot-Aktion vor oder nach und nie innerhalb einer bestimmten Gruppe von Aktionen in den Aktionssequenztabellen platziert wird. Im Thema ForceReboot action (ForceReboot-Aktion) finden Sie Informationen zu den Aktionen, aus denen diese Gruppe besteht.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cda8676a072ebed21a16653dca9af67464f35699530eb3c08ae05d3cd9574b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528780"
---
# <a name="ice28"></a>ICE28

ICE28 wird häufig verwendet, um zu überprüfen, ob die ForceReboot-Aktion vor oder nach und nie innerhalb einer bestimmten Gruppe von Aktionen in den Aktionssequenztabellen platziert wird. Im Thema [ForceReboot action (ForceReboot-Aktion)](forcereboot-action.md) finden Sie Informationen zu den Aktionen, aus denen diese Gruppe besteht.

ICE28 überprüft Aktionen in den folgenden Sequenztabellen:

[AdminUISequence-Tabelle](adminuisequence-table.md)

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)

[InstallUISequence-Tabelle](installuisequence-table.md)

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)

## <a name="result"></a>Ergebnis

ICE28 sendet eine Fehlermeldung, wenn ForceReboot innerhalb der angegebenen Aktionsgruppe sequenziert ist.

## <a name="example"></a>Beispiel

Für das gezeigte Beispiel sendet ICE28 die folgende Fehlermeldung:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion             | Sequenz |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

Die Sequenznummer 10 für ForceReboot-Unterbrechungen generiert den Fehler, da er zwischen den Sequenznummern von RegisterMIMEInfo und RegisterProgIdInfo liegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



