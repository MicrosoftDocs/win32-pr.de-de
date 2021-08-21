---
description: Der bekannte Bezeichner \_ \_ CLASS bezieht sich auf eine Pseudoeigenschaft für jedes WMI-Objekt, das die Klasse des aktuellen Objekts angibt.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: __CLASS-Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f40d95d0476bf139aebd3cc6eefe8a34782a48bec311f2a40e1f861ec27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110744"
---
# <a name="__class-identifier"></a>\_\_KLASSENbezeichner

Der bekannte Bezeichner \_ \_ CLASS bezieht sich auf eine Pseudoeigenschaft für jedes WMI-Objekt, das die Klasse des aktuellen Objekts angibt.

Verwenden Sie \_ \_ CLASS in einer [WHERE-Klausel,](where-clause.md) um objekte abgeleiteter Klassen aus dem Resultset herauszufiltern. Das Resultset der folgenden Abfrage enthält beispielsweise nicht nur Objekte, deren Klasse [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)ist, sondern auch Objekte, deren Klasse von **Win32 \_ LogicalDisk** abgeleitet ist.


```sql
SELECT * FROM Win32_LogicalDisk
```



Im folgenden Beispiel filtert die Verwendung von \_ \_ CLASS in der **WHERE-Klausel** alle Objekte von Klassen heraus, die von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) abgeleitet wurden, da ihre Klasse nicht **Win32 \_ LogicalDisk** ist.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Verwenden Sie \_ \_ CLASS in Anbietern, die aufgefordert werden, Instanzen einer bestimmten Klasse unabhängig von Unterklassen bereitzustellen.

 

 
