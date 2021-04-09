---
description: ICE28 wird häufig verwendet, um zu überprüfen, ob die ForceReboot-Aktion vor oder nach und nie innerhalb einer bestimmten Gruppe von Aktionen in den Aktions Sequenz Tabellen platziert wird. Informationen zu den Aktionen, aus denen diese Gruppe besteht, finden Sie im Thema "ForceReboot Action".
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750129"
---
# <a name="ice28"></a>ICE28

ICE28 wird häufig verwendet, um zu überprüfen, ob die ForceReboot-Aktion vor oder nach und nie innerhalb einer bestimmten Gruppe von Aktionen in den Aktions Sequenz Tabellen platziert wird. Informationen zu den Aktionen, aus denen diese Gruppe besteht, finden Sie im Thema " [ForceReboot Action](forcereboot-action.md) ".

ICE28 überprüft Aktionen in den folgenden Sequenz Tabellen:

[AdminUISequence-Tabelle](adminuisequence-table.md)

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)

[InstallUISequence-Tabelle](installuisequence-table.md)

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)

## <a name="result"></a>Ergebnis

ICE28 gibt eine Fehlermeldung aus, wenn ForceReboot innerhalb der angegebenen Aktionsgruppe sequenziert wird.

## <a name="example"></a>Beispiel

Im gezeigten Beispiel gibt ICE28 die folgende Fehlermeldung aus:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion             | Sequenz |
|--------------------|----------|
| ForceReboot        | 10       |
| Registermimeinfo   |   5      |
| Registerprogidinfo | 15       |



 

Die Sequenznummer 10, die für ForceReboot-Unterbrechungen angegeben wird, generiert den Fehler, da Sie zwischen den Sequenznummern von registermimeinfo und registerprogidinfo liegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



