---
description: ICE72 überprüft, ob nicht integrierte benutzerdefinierte Aktionen in der AdvtExecuteSequence-Tabelle nicht verwendet werden.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368978"
---
# <a name="ice72"></a>ICE72

ICE72 überprüft, ob nicht integrierte benutzerdefinierte Aktionen in der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)nicht verwendet werden. Insbesondere sind in der AdvtExecuteSequence-Tabelle nur benutzerdefinierte Aktionen vom Typ 19, Typ 35 und Type 51 zulässig. Wenn andere benutzerdefinierte Aktionen verwendet werden, verhält sich die Ankündigung möglicherweise nicht wie erwartet.

## <a name="result"></a>Ergebnis

ICE72 gibt einen Fehler zurück, wenn die advexecutesequence-Tabelle andere benutzerdefinierte Aktionen als den Typ 35, den Typ 51 und den Typ 19 verwendet.

## <a name="example"></a>Beispiel

ICE72 meldet den folgenden Fehler für das gezeigte Beispiel:

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Entfernen Sie "CA1" aus der AdvtExecuteSequence-Tabelle, um den Fehler zu beheben.

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



 

## <a name="tables-used-during-execution"></a>Während der Ausführung verwendete Tabellen

[AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)

[Tabelle "CustomAction"](customaction-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierter Aktionstyp 19](custom-action-type-19.md)
</dt> <dt>

[Benutzerdefinierter Aktionstyp 35](custom-action-type-35.md)
</dt> <dt>

[Benutzerdefinierter Aktionstyp 51](custom-action-type-51.md)
</dt> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



