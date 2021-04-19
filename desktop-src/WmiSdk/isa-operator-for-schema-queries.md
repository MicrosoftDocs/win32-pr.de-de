---
description: Der ISA-Operator ist ein WQL-spezifischer Operator, der in Daten-, Ereignis-und Schema Abfragen verwendet werden kann.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: ISA-Operator für Schema Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359183"
---
# <a name="isa-operator-for-schema-queries"></a><span data-ttu-id="ca22f-103">ISA-Operator für Schema Abfragen</span><span class="sxs-lookup"><span data-stu-id="ca22f-103">ISA Operator for Schema Queries</span></span>

<span data-ttu-id="ca22f-104">Der ISA-Operator ist ein WQL-spezifischer Operator, der in Daten-, Ereignis-und Schema Abfragen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca22f-104">The ISA operator is a WQL-specific operator that can be used in data, event, and schema queries.</span></span>

<span data-ttu-id="ca22f-105">Wenn ISA in der WHERE- [Klausel](where-clause.md) einer Schema Abfrage enthalten ist, wird angefordert, dass die Abfrage auf alle Unterklassen der von Ihnen angegebenen Klasse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca22f-105">When ISA is included in the [WHERE clause](where-clause.md) of an schema query, it requests that the query be applied to all subclasses of the class you specify.</span></span>

<span data-ttu-id="ca22f-106">Die folgende Anweisung fordert z. b. alle 10 Minuten eine Benachrichtigung mit instanzänderungsereignissen für alle Instanzen an, die Mitglieder einer beliebigen Klasse sind, die von der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ca22f-106">For example, the following statement requests notification every 10 minutes of instance modification events for all instances that are members of any class deriving from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="ca22f-107">Die folgende Abfrage gibt die Definition für die [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor) Klasse und Definitionen für alle zugehörigen Unterklassen zurück.</span><span class="sxs-lookup"><span data-stu-id="ca22f-107">The following query returns the definition for the [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor) class and definitions for all of its subclasses.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



<span data-ttu-id="ca22f-108">Die Klasse **Meta \_ Class** identifiziert dies als Schema Abfrage, die Eigenschaft, die **\_ \_ als bezeichnet wird** , die Zielklasse der Abfrage, und der ISA-Operator fordert Definitionen für die Unterklassen der Zielklasse an.</span><span class="sxs-lookup"><span data-stu-id="ca22f-108">The class **meta\_class** identifies this as a schema query, the property called **\_\_this** identifies the target class of the query, and the ISA operator requests definitions for the subclasses of the target class.</span></span>

 

 
