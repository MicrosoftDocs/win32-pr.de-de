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
# <a name="isa-operator-for-schema-queries"></a>ISA-Operator für Schema Abfragen

Der ISA-Operator ist ein WQL-spezifischer Operator, der in Daten-, Ereignis-und Schema Abfragen verwendet werden kann.

Wenn ISA in der WHERE- [Klausel](where-clause.md) einer Schema Abfrage enthalten ist, wird angefordert, dass die Abfrage auf alle Unterklassen der von Ihnen angegebenen Klasse angewendet wird.

Die folgende Anweisung fordert z. b. alle 10 Minuten eine Benachrichtigung mit instanzänderungsereignissen für alle Instanzen an, die Mitglieder einer beliebigen Klasse sind, die von der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse abgeleitet wird.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Die folgende Abfrage gibt die Definition für die [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor) Klasse und Definitionen für alle zugehörigen Unterklassen zurück.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



Die Klasse **Meta \_ Class** identifiziert dies als Schema Abfrage, die Eigenschaft, die **\_ \_ als bezeichnet wird** , die Zielklasse der Abfrage, und der ISA-Operator fordert Definitionen für die Unterklassen der Zielklasse an.

 

 
