---
title: Suchen von Objekten nach Klasse
description: Eine typische Suchabfrage für eine bestimmte Objektklasse.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Suchen von Objekten nach Klasse AD
- Active Directory, using, searching, by class
- Object AD , Suchen nach Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d90dbcd50a3ce001c1dec57d8fafb0f1987376cf71314902b7f035f923512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189169"
---
# <a name="finding-objects-by-class"></a>Suchen von Objekten nach Klasse

Eine typische Suchabfrage für eine bestimmte Objektklasse. Im folgenden Codebeispiel wird nach Computern mit Standort in Building 7N gesucht.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Überlegen Sie, warum **objectClass** nicht verwendet wird. Verwenden Sie **objectClass** nicht ohne einen anderen Vergleich, der ein indiziertes Attribut enthält. Indexattribute können die Effizienz einer Abfrage erhöhen. Das **objectClass-Attribut** ist mehrwertiger und nicht indiziert. Verwenden Sie **objectCategory,** um den Typ oder die Klasse eines Objekts anzugeben.

Weniger effizient:


```C++
(objectClass=computer)
```



Effizienter:


```C++
(objectCategory=computer)
```



Beachten Sie, dass in einigen Fällen eine Kombination aus **objectClass** und **objectCategory** verwendet werden muss. Die Benutzerklasse und die Kontaktklasse sollten wie folgt angegeben werden.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Beachten Sie, dass Sie mit den folgenden Informationen sowohl nach Benutzern als auch nach Kontakten suchen können.


```C++
(objectCategory=person)
```



 

 




