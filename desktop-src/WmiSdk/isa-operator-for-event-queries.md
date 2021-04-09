---
description: Der ISA-Operator ist ein WQL-spezifischer Operator, der in Ereignis Abfragen verwendet werden kann. Wenn ISA in der WHERE-Klausel einer Ereignis Abfrage enthalten ist, wird eine Benachrichtigung über Ereignisse für alle Klassen in einer Klassenhierarchie und nicht für eine bestimmte Ereignisklasse angefordert.
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: ISA-Operator für Ereignis Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042681"
---
# <a name="isa-operator-for-event-queries"></a>ISA-Operator für Ereignis Abfragen

Der ISA-Operator ist ein WQL-spezifischer Operator, der in Ereignis Abfragen verwendet werden kann. Wenn ISA in der WHERE- [Klausel](where-clause.md) einer Ereignis Abfrage enthalten ist, wird eine Benachrichtigung über Ereignisse für alle Klassen in einer Klassenhierarchie und nicht für eine bestimmte Ereignisklasse angefordert.

Im folgenden Beispiel wird die Benachrichtigung alle 10 Minuten mit instanzänderungsereignissen für alle Instanzen angefordert, die Mitglieder einer beliebigen Klasse sind, die von der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse abgeleitet ist.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Weitere Informationen zur Verwendung von ISA mit einer Ereignis Abfrage finden Sie unter [Erstellen eines Zeit Geber Ereignisses mit Win32 \_ localtime oder Win32 \_ utcTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

 

 
