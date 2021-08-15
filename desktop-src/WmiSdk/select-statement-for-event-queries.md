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

Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Ereignisinformationen abfragt. Bei den Anweisungen kann es sich um einfache Anweisungen oder um restriktivere Anweisungen zum Einschränken des von der Abfrage zurückgegebenen Ergebnisses handelt.

Das folgende Beispiel ist eine einfache SELECT-Anweisung, die zum Abfragen von Ereignisinformationen verwendet wird.


```sql
SELECT * FROM EventClass
```



Wenn ein Consumer eine Abfrage übermittelt, ist es eine Anforderung, über alle Vorkommen des Ereignisses benachrichtigt zu werden, das durch **EventClass dargestellt wird.** Diese Anforderung enthält eine Anforderung zur Benachrichtigung über alle Ereignissystem- und Nichtsystemeigenschaften. Wenn ein Ereignisanbieter eine Abfrage übermittelt, registriert er Unterstützung für das Generieren von Benachrichtigungen, wenn ein durch **EventClass** dargestelltes Ereignis auftritt.

Consumers können einzelne Eigenschaften anstelle des Sternchens ( \* ) in der SELECT-Anweisung angeben.

Das folgende Beispiel zeigt, wie sie bestimmte Eigenschaften abfragen.


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



Wenn eine Systemeigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält sie **NULL.** Beispielsweise ist der Wert der **\_ \_ RELPATH-Systemeigenschaft** **für alle** Ereignisabfragen NULL.

Die folgenden Systemeigenschaften enthalten **NULL für** Ereignisabfragen:

<dl> \_\_Namespace  
\_\_Pfad  
\_\_RelPath  
\_\_Server  
</dl>

Weitere Informationen finden Sie unter [WMI-Systemeigenschaftsreferenz.](wmi-system-properties.md)

Alle Ereignisabfragen können eine optionale [WHERE-Klausel enthalten.](where-clause.md)WHERE-Klauseln werden jedoch in erster Linie von Consumers verwendet, um zusätzliche Filter anzugeben. Es wird dringend empfohlen, dass Benutzer immer eine WHERE-Klausel angeben. Die Kosten einer komplexen Abfrage sind im Vergleich zu den Kosten für die Bereitstellung und Verarbeitung nicht verwendeter Benachrichtigungen minimal.

Das folgende Beispiel zeigt eine Abfrage, die Benachrichtigungen über alle Instanzänderungsereignisse anfragt, die sich auf die hypothetische Klasse **EmailEvent auswirken.**


```sql
SELECT * FROM EmailEvent
```



Wenn Ereignisse im Zusammenhang **mit EmailEvent** häufig auftreten, wird der Consumer mit Ereignissen überflutet. Eine bessere Abfrage fordert Ereignisse nur an, wenn bestimmte Bedingungen Eigenschaften der angegebenen Klasse verwenden, z. B. wenn die Wichtigkeitsstufe hoch ist.

Das folgende Beispiel zeigt die Abfrage, die Sie verwenden können, **wenn EmailImportance** eine Eigenschaft der Klasse **EmailEvent ist.**


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Beachten Sie, dass WMI eine Abfrage aus verschiedenen Gründen ablehnen kann. Beispielsweise kann die Abfrage zu komplex oder ressourcenintensiv für die Auswertung sein. In diesem Fall gibt WMI bestimmte Fehlercodes zurück, z. **B. WBEM \_ E INVALID \_ \_ QUERY**.

Eigenschaften eingebetteter Objekte können in der WHERE-Klausel verwendet werden.

Im folgenden Beispiel wird gezeigt, wie Sie Objekte abfragen, bei denen die **TargetInstance-Eigenschaft** der [**\_ \_ InstanceModificationEvent-Systemklasse**](--instancemodificationevent.md) ein eingebettetes [**Win32 \_ LogicalDisk-Objekt**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) und **FreeSpace** eine Eigenschaft von **Win32 \_ LogicalDisk ist.**


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Beispiele

Das VbScript-Beispiel monitor creation event [for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) (Überwachung der Erstellung eines bestimmten Prozessnamens) auf TechNet verwendet die SELECT-Anweisung, um WMI-Instanzerstellungsereignisse für den Win32-Prozess zu überwachen und nach einem bestimmten \_ Prozessnamen zu filtern.

 

 
