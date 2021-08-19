---
description: ICE72 überprüft, ob nicht integrierte benutzerdefinierte Aktionen in der Tabelle AdvtExecuteSequence nicht verwendet werden.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f931e705dbca734348f62ba4b1ca106b43bb80a52c50f0e94ecab7139c624da2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946577"
---
# <a name="ice72"></a>ICE72

ICE72 überprüft, ob nicht integrierte benutzerdefinierte Aktionen in der [Tabelle AdvtExecuteSequence](advtexecutesequence-table.md)nicht verwendet werden. Insbesondere sind nur der Typ 19, der Typ 35 und der Typ 51 benutzerdefinierte Aktionen in der Tabelle AdvtExecuteSequence zulässig. Wenn andere benutzerdefinierte Aktionen verwendet werden, verhält sich die Ankündigung möglicherweise nicht wie erwartet.

## <a name="result"></a>Ergebnis

ICE72 gibt einen Fehler zurück, wenn die Tabelle AdvExecuteSequence andere benutzerdefinierte Aktionen als typ 35, type 51 und type 19 verwendet.

## <a name="example"></a>Beispiel

ICE72 meldet den folgenden Fehler für das gezeigte Beispiel:

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Entfernen Sie "CA1" aus der Tabelle AdvtExecuteSequence, um den Fehler zu beheben.

[AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) (partiell)



| Aktion |
|--------|
| KA1    |
| CA35   |



 

[CustomAction-Tabelle](customaction-table.md) (partiell)



| Aktion | type |
|--------|------|
| KA1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>Tabellen, die während der Ausführung verwendet werden

[Tabelle "AdvtExecuteSequence"](advtexecutesequence-table.md)

[CustomAction-Tabelle](customaction-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierter Aktionstyp 19](custom-action-type-19.md)
</dt> <dt>

[Benutzerdefinierter Aktionstyp 35](custom-action-type-35.md)
</dt> <dt>

[Benutzerdefinierter Aktionstyp 51](custom-action-type-51.md)
</dt> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



