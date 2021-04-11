---
description: Die bekannte \_ \_ bezeichnerklasse verweist auf eine Pseudo Eigenschaft auf jedem WMI-Objekt, das die Klasse des aktuellen-Objekts angibt.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: __CLASS Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131776"
---
# <a name="__class-identifier"></a>\_\_Klassen Bezeichner

Die bekannte \_ \_ bezeichnerklasse verweist auf eine Pseudo Eigenschaft auf jedem WMI-Objekt, das die Klasse des aktuellen-Objekts angibt.

Verwenden Sie \_ \_ die-Klasse in einer [Where](where-clause.md) -Klausel, um alle Objekte abgeleiteter Klassen aus dem Resultset herauszufiltern. Das Resultset der folgenden Abfrage enthält z. b. nicht nur Objekte, deren Klasse [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)ist, sondern auch Objekte, deren Klasse von **Win32 \_ LogicalDisk** abgeleitet ist.


```sql
SELECT * FROM Win32_LogicalDisk
```



Im folgenden Beispiel filtert die Verwendung der- \_ \_ Klasse in der **Where** -Klausel alle Objekte von Klassen, die von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) abgeleitet werden, da Ihre Klasse nicht **Win32 \_ LogicalDisk** ist.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Verwenden \_ \_ Sie die-Klasse in Anbietern, die zur Bereitstellung von Instanzen einer bestimmten Klasse aufgefordert werden, unabhängig von den Unterklassen.

 

 
