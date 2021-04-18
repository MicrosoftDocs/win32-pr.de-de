---
title: Suchen nach Objekten nach Klasse
description: Eine typische Suchabfrage für eine bestimmte Objektklasse.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Suchen nach Objekten nach Klasse AD
- Active Directory, verwenden, suchen, nach Klasse
- Objekt-AD, Suche nach Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337754"
---
# <a name="finding-objects-by-class"></a>Suchen nach Objekten nach Klasse

Eine typische Suchabfrage für eine bestimmte Objektklasse. Im folgenden Codebeispiel wird nach Computern mit dem Standort in der Gebäude 7N gesucht.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Bedenken Sie, warum **objectClass** nicht verwendet wird. Verwenden Sie **objectClass** nicht ohne einen anderen Vergleich, der ein indiziertes Attribut enthält. Index Attribute können die Effizienz einer Abfrage erhöhen. Das **objectClass** -Attribut ist mehr wertig und nicht indiziert. Verwenden Sie **objectCategory**, um den Typ oder die Klasse eines Objekts anzugeben.

Weniger effizient:


```C++
(objectClass=computer)
```



Effizienter:


```C++
(objectCategory=computer)
```



Beachten Sie, dass es einige Fälle gibt, in denen eine Kombination aus " **objectClass** " und " **objectCategory** " verwendet werden muss. Die User-Klasse und die Contact-Klasse sollten wie folgt angegeben werden.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Beachten Sie, dass Sie mit den folgenden Benutzern und Kontakten nach Benutzern und Kontakten suchen können.


```C++
(objectCategory=person)
```



 

 




