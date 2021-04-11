---
description: 'Weitere Informationen finden Sie unter: Order By-Klausel.'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: ORDER BY-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128536"
---
# <a name="order-by-clause"></a>ORDER BY-Klausel

Die Order By-Klausel sortiert die Ergebnisse basierend auf dem Wert einer oder mehrerer Spalten, die Sie angeben. Im folgenden finden Sie die Syntax der ORDER BY-Klausel:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



Der Spaltenspezifizierer muss eine gültige Spalte sein. Sie können den Spalten Bezeichner verwenden, um auf Spalten in der Reihenfolge zu verweisen, in der Sie in der Abfrage angezeigt werden. Die erste Spalte in der Abfrage wird mit 1 nummeriert. Sie können mehr als eine Spalte in der ORDER BY-Klausel einschließen, getrennt durch Kommas.

Der optionale richtungsspezifizierer kann entweder "ASC" für aufsteigend (niedrig zu hoch) oder "absteigend" (hoch bis niedrig) sein. Wenn Sie keinen richtungsspezifizierer angeben, wird der Standardwert aufsteigend verwendet. Wenn Sie mehr als eine Spalte angeben, aber nicht alle Richtungen angeben, wird die von Ihnen angegebene Richtung auf jede Spalte angewendet, bis Sie die Richtung explizit ändern.

In der folgenden Order By-Klausel werden z. B. die Spalten A, B, C und G in aufsteigender Reihenfolge sortiert, während die Spalten D, E und F in absteigender Reihenfolge sortiert werden.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[FROM-Klausel](-search-sql-from.md)
</dt> <dt>

[Rank by-Klausel](-search-sql-rankby.md)
</dt> <dt>

[SELECT-Anweisung](-search-sql-select.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



