---
title: Suchen von Objekten nach Namen
description: Die meisten Objekte in Active Directory Domain Services verwenden die cn-Eigenschaft als Benennungsattribut.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, suchen, nach Namen
- Object AD , Suchen nach Namen
- Suchen von Objekten nach Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60624c62e9d28d35805af3c98f551a19f44edf9e27369cf7ded9e87621491cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189180"
---
# <a name="finding-objects-by-name"></a>Suchen von Objekten nach Namen

Die meisten Objekte in Active Directory Domain Services die **cn-Eigenschaft** als Benennungsattribut verwenden. Einige Objekte verwenden jedoch ein anderes Benennungsattribut als **cn.** Beispielsweise verwendet ein Domänencontroller die **domainDNS-Eigenschaft** für das Naming-Attribut, und eine Organisationseinheit verwendet die **organizationalUnit-Eigenschaft** für das Naming-Attribut. Um zu vermeiden, dass ein anderes Benennungsattribut für verschiedene Objekttypen verwendet werden muss, sollte die **Name-Eigenschaft,** die den relativen Distinguished Name des Objekts enthält, verwendet werden, um nach Objekten nach Namen zu suchen.

## <a name="examples"></a>Beispiele

Die folgenden Codebeispiele zeigen verschiedene Abfragezeichenfolgen, die zum Suchen von Objekten anhand des Namens verwendet werden können.

Die folgende Abfragezeichenfolge sucht alle Objekte mit einem Namen, der mit "Jeff" beginnt.


```C++
(name=Jeff*)
```



Die folgende Abfragezeichenfolge sucht alle Computerobjekte mit einem Namen, der mit "leased" oder "corp" beginnt.


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



Die folgende Abfragezeichenfolge sucht alle Benutzer und mit einem Namen, der mit "Karen" oder "Jeff" beginnt.


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




