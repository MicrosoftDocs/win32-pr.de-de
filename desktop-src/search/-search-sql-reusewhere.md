---
description: Die WHERE-Klausel in einer Abfrage gibt eine Menge von Elementen an, mit denen die Ergebnisse verglichen werden sollen.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Reusewhere-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353025"
---
# <a name="reusewhere-function"></a>Reusewhere-Funktion

Die [Where](-search-sql-where.md) -Klausel in einer Abfrage gibt eine Menge von Elementen an, mit denen die Ergebnisse verglichen werden sollen. Nachfolgende Abfragen können die Arbeit, die für eine vorherige Abfrage ausgeführt wird, mithilfe der reusewhere-Funktion in einer neuen Abfrage in der WHERE-Klausel freigeben. Abfragen, die diese Funktion nutzen, werden schneller ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Szenario wird gezeigt, wie die reusewhere-Funktion verwendet wird:

1.  Sie geben die folgende Abfrage aus:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  Aus dem zurückgegebenen Rowset erhalten Sie eine [Where-ID](-search-sql-rowset-properties.md), *Query1WhereID*.

    Die WHERE-ID ist eine Rowseteigenschaft mit dem propset {aa6ee6b0-E828-11D0-B2-3E-00-AA-00-47-FC-01}, PROPID 8 und Type UI4.

3.  Sie geben eine zweite Abfrage mit der reusewhere-Funktion aus und übergeben dabei den *Query1WhereID* aus Schritt 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

Die zweite Abfrage entspricht Folgendem:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



Die reusewhere-Funktion kann in der [Where](-search-sql-where.md) -Klausel verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

[Rowset-Eigenschaften](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



