---
description: Die WHERE-Klausel in einer Abfrage gibt einen Satz von Elementen an, mit denen Ergebnisse übereinstimmen.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f073a7ac0d5faf5973d08ff53ccebdacf8bead080a53e2d9a4a6ae9ed5724db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944660"
---
# <a name="reusewhere-function"></a>ReuseWhere-Funktion

Die [WHERE-Klausel](-search-sql-where.md) in einer Abfrage gibt einen Satz von Elementen an, mit denen Ergebnisse übereinstimmen. Nachfolgende Abfragen können die Für eine vorherige Abfrage ausgeführte Arbeit mithilfe der ReuseWhere-Funktion in einer neuen WHERE-Abfrageklausel gemeinsam nutzen. Abfragen, die diese Funktion nutzen, werden schneller ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Szenario wird die Verwendung der ReuseWhere-Funktion veranschaulicht:

1.  Sie stellen die folgende Abfrage aus:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  Aus dem zurückgegebenen Rowset erhalten Sie where [ID](-search-sql-rowset-properties.md), *Query1WhereID*.

    Die Where-ID ist eine Rowseteigenschaft mit PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8 und Typ UI4.

3.  Sie geben eine zweite Abfrage mit der ReuseWhere-Funktion aus und übergeben die *Query1WhereID* aus Schritt 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

Die zweite Abfrage entspricht der folgenden:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



Die ReuseWhere-Funktion kann in der [WHERE-Klausel](-search-sql-where.md) anwhere verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

[Rowset-Eigenschaften](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



