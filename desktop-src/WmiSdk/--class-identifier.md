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
# <a name="__class-identifier"></a><span data-ttu-id="ec843-103">\_\_Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ec843-103">\_\_CLASS Identifier</span></span>

<span data-ttu-id="ec843-104">Die bekannte \_ \_ bezeichnerklasse verweist auf eine Pseudo Eigenschaft auf jedem WMI-Objekt, das die Klasse des aktuellen-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="ec843-104">The well-known identifier \_\_CLASS refers to a pseudo-property on every WMI object that indicates the class of the current object.</span></span>

<span data-ttu-id="ec843-105">Verwenden Sie \_ \_ die-Klasse in einer [Where](where-clause.md) -Klausel, um alle Objekte abgeleiteter Klassen aus dem Resultset herauszufiltern.</span><span class="sxs-lookup"><span data-stu-id="ec843-105">Use \_\_CLASS in a [WHERE](where-clause.md) clause to filter out any objects of derived classes from your result set.</span></span> <span data-ttu-id="ec843-106">Das Resultset der folgenden Abfrage enthält z. b. nicht nur Objekte, deren Klasse [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)ist, sondern auch Objekte, deren Klasse von **Win32 \_ LogicalDisk** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="ec843-106">For example, the result set of the following query contains not only objects whose class is [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), but also objects whose class is derived from **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk
```



<span data-ttu-id="ec843-107">Im folgenden Beispiel filtert die Verwendung der- \_ \_ Klasse in der **Where** -Klausel alle Objekte von Klassen, die von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) abgeleitet werden, da Ihre Klasse nicht **Win32 \_ LogicalDisk** ist.</span><span class="sxs-lookup"><span data-stu-id="ec843-107">In the following example, the use of \_\_CLASS in the **WHERE** clause filters out all objects of classes derived from [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) because their class is not **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



<span data-ttu-id="ec843-108">Verwenden \_ \_ Sie die-Klasse in Anbietern, die zur Bereitstellung von Instanzen einer bestimmten Klasse aufgefordert werden, unabhängig von den Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="ec843-108">Use \_\_CLASS in providers that are asked to provide instances of a specific class, irrespective of any subclasses.</span></span>

 

 
