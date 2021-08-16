---
description: Weitere Informationen finden Sie unter ORDER BY-Klausel.
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: ORDER BY-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3815ddecc659a47d7cf2c8547b49e878c54ba6bf8537e2589eea4441d9d3f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227185"
---
# <a name="order-by-clause"></a>ORDER BY-Klausel

Die ORDER BY-Klausel sortiert die Ergebnisse basierend auf dem Wert einer oder mehrere Spalten, die Sie angeben. Es folgt die Syntax der ORDER BY-Klausel:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



Der Spaltenspezifizierer muss eine gültige Spalte sein. Sie können den Spaltenspezifizierer verwenden, um in der Reihenfolge, in der sie in der Abfrage angezeigt werden, auf Spalten zu verweisen. Die erste Spalte in der Abfrage ist mit 1 nummeriert. Sie können mehr als eine Spalte in die ORDER BY-Klausel durch Kommas getrennt hinzufügen.

Der optionale Richtungsspezifizierer kann entweder "ASC" für aufsteigend (niedrig bis hoch) oder "DESC" für absteigend (hoch bis niedrig) sein. Wenn Sie keinen Richtungsspezifizierer bereitstellen, wird der Standardwert (aufsteigend) verwendet. Wenn Sie mehrere Spalten angeben, aber nicht alle Richtungen angeben, wird die Richtung, die Sie zuletzt angeben, auf jede Spalte angewendet, bis Sie die Richtung explizit ändern.

In der folgenden ORDER BY-Klausel werden beispielsweise die Spalten A, B, C und G in aufsteigender Reihenfolge sortiert, während die Spalten D, E und F in absteigender Reihenfolge sortiert werden.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[FROM-Klausel](-search-sql-from.md)
</dt> <dt>

[RANK BY-Klausel](-search-sql-rankby.md)
</dt> <dt>

[SELECT-Anweisung](-search-sql-select.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltext-Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltext-Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



