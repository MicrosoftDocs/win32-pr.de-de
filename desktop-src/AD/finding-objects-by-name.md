---
title: Suchen nach Objekten nach Namen
description: Die meisten Objekte in Active Directory Domain Services die CN-Eigenschaft als Benennungs Attribut verwenden.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, suchen, nach Namen
- Objekt-AD, Suche nach Name
- Suchen nach Objekten nach Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707619"
---
# <a name="finding-objects-by-name"></a>Suchen nach Objekten nach Namen

Die meisten Objekte in Active Directory Domain Services die **CN** -Eigenschaft als Benennungs Attribut verwenden. Einige Objekte verwenden jedoch ein anderes Namensattribut als **CN**. Ein Domänen Controller verwendet beispielsweise die **domainDns** -Eigenschaft für das Naming-Attribut, und eine Organisationseinheit verwendet die **OrganizationalUnit** -Eigenschaft für das Naming-Attribut. Um zu vermeiden, dass ein anderes Naming-Attribut für verschiedene Objekttypen verwendet werden muss, sollte die **Name** -Eigenschaft, die den relativen Distinguished Name des Objekts enthält, für die Suche nach Objekten nach Namen verwendet werden.

## <a name="examples"></a>Beispiele

Die folgenden Codebeispiele zeigen verschiedene Abfrage Zeichenfolgen, die verwendet werden können, um Objekte nach Namen zu suchen.

Die folgende Abfrage Zeichenfolge findet alle Objekte mit einem Namen, der mit "Jeff" beginnt.


```C++
(name=Jeff*)
```



Die folgende Abfrage Zeichenfolge findet alle Computer Objekte mit einem Namen, der mit "geleast" oder "Corp" beginnt.


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



Die folgende Abfrage Zeichenfolge findet alle Benutzer und mit einem Namen, der mit "Karen" oder "Jeff" beginnt.


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




