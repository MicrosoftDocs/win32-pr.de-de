---
description: Beschreibt die grundlegende Syntax einer SELECT-Anweisung für Ereignisabfragen.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: SELECT-Anweisung für Ereignisabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e36eaa8f396f8dd7b7c0b0c013d1d6738fefeb7ed2ae565ee7114ebb524faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315839"
---
# <a name="select-statement-for-event-queries"></a>SELECT-Anweisung für Ereignisabfragen

Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Ereignisinformationen abzufragen. Die Anweisungen können einfache Anweisungen oder restriktiver sein, um das von der Abfrage zurückgegebene Resultset einzugrenzen.

Das folgende Beispiel ist eine einfache SELECT-Anweisung, die zum Abfragen von Ereignisinformationen verwendet wird.


```sql
SELECT * FROM EventClass
```



Wenn ein Consumer eine Abfrage übermittelt, ist es eine Anforderung, über alle Vorkommen des ereignisses benachrichtigt zu werden, das durch **EventClass** dargestellt wird. Diese Anforderung enthält eine Anforderung zur Benachrichtigung über alle Ereignissystem- und Nichtsystemeigenschaften. Wenn ein Ereignisanbieter eine Abfrage übermittelt, registriert er Unterstützung für das Generieren von Benachrichtigungen, wenn ein durch **EventClass** dargestelltes Ereignis auftritt.

Consumer können einzelne Eigenschaften anstelle des Sternchens \* () in der SELECT-Anweisung angeben.

Im folgenden Beispiel wird veranschaulicht, wie bestimmte Eigenschaften abgefragt werden.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Allerdings werden alle Eigenschaften eines eingebetteten Objekts zurückgegeben, auch wenn die Abfrage eingebettete Objekteigenschaften angibt.

Das folgende Beispiel zeigt zwei Abfragen, die die gleichen Daten zurückgeben.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Wenn eine Systemeigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält sie **NULL.** Beispielsweise ist der Wert der **\_ \_ RELPATH-Systemeigenschaft** für alle Ereignisabfragen **NULL.**

Die folgenden Systemeigenschaften enthalten **NULL** für Ereignisabfragen:

<dl> \_\_Namespace  
\_\_Pfad  
\_\_RelPath  
\_\_Server  
</dl>

Weitere Informationen finden Sie unter [WMI-Systemeigenschaftenreferenz.](wmi-system-properties.md)

Alle Ereignisabfragen können eine optionale [WHERE-Klausel](where-clause.md)enthalten. WHERE-Klauseln werden jedoch hauptsächlich von Consumern verwendet, um zusätzliche Filter anzugeben. Es wird dringend empfohlen, dass Consumer immer eine WHERE-Klausel angeben. Die Kosten einer komplexen Abfrage sind im Vergleich zu den Kosten für die Übermittlung und Verarbeitung nicht benötigter Benachrichtigungen minimal.

Das folgende Beispiel zeigt eine Abfrage, die Benachrichtigungen über alle Instanzänderungsereignisse anfordert, die sich auf die hypothetische **Klasse EmailEvent** auswirken.


```sql
SELECT * FROM EmailEvent
```



Wenn Ereignisse im Zusammenhang mit **EmailEvent** häufig auftreten, wird der Consumer mit Ereignissen überflutet. Eine bessere Abfrage fordert Ereignisse nur dann an, wenn bestimmte Bedingungen Eigenschaften der angegebenen Klasse verwenden, z. B. wenn die Wichtigkeitsstufe hoch ist.

Das folgende Beispiel zeigt die Abfrage, die Sie verwenden können, wenn **EmailImportance** eine Eigenschaft der **Klasse EmailEvent** ist.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Beachten Sie, dass WMI eine Abfrage aus verschiedenen Gründen ablehnen kann. Beispielsweise kann die Abfrage zu komplex oder ressourcenintensiv für die Auswertung sein. In diesem Fall gibt WMI bestimmte Fehlercodes zurück, z. B. **WBEM \_ E \_ INVALID \_ QUERY**.

Eigenschaften eingebetteter Objekte können in der WHERE-Klausel verwendet werden.

Das folgende Beispiel zeigt, wie Nach -Objekten abgefragt wird, bei denen die **TargetInstance-Eigenschaft** der [**\_ \_ InstanceModificationEvent-Systemklasse**](--instancemodificationevent.md) ein eingebettetes [**Win32 \_ LogicalDisk-Objekt**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) und **FreeSpace** eine Eigenschaft von **Win32 \_ LogicalDisk** ist.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Beispiele

Das Beispiel Monitor creation event for specific process name VBScript on TechNet [(Monitorerstellungsereignis für einen bestimmten Prozessnamen)](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) auf TechNet verwendet die SELECT-Anweisung, um Die Erstellungsereignisse der WMI-Instanz für win32 Process zu überwachen \_ und nach einem bestimmten Prozessnamen zu filtern.

 

 
