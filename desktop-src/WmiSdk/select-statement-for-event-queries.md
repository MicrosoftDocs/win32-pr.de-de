---
description: Beschreibt die grundlegende Syntax einer SELECT-Anweisung für Ereignis Abfragen.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: SELECT-Anweisung für Ereignis Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217956"
---
# <a name="select-statement-for-event-queries"></a>SELECT-Anweisung für Ereignis Abfragen

Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Ereignis Informationen abzufragen. Die Anweisungen können einfache Anweisungen sein, oder Sie können restriktiver sein, um das Resultset einzugrenzen, das von der Abfrage zurückgegeben wird.

Das folgende Beispiel ist eine einfache SELECT-Anweisung, die verwendet wird, um Ereignis Informationen abzufragen.


```sql
SELECT * FROM EventClass
```



Wenn ein Consumer eine Abfrage übermittelt, ist es eine Anforderung, über alle Vorkommen des Ereignisses benachrichtigt zu werden, die von **EventClass** dargestellt werden. Diese Anforderung enthält eine Benachrichtigungs Anforderung zu allen Ereignis System-und nicht-Systemeigenschaften. Wenn ein Ereignis Anbieter eine Abfrage übermittelt, registriert er die Unterstützung für das Erstellen von Benachrichtigungen, wenn ein Ereignis auftritt, das von **EventClass** dargestellt wird.

Consumer können einzelne Eigenschaften anstelle des Sternchen ( \* ) in der SELECT-Anweisung angeben.

Im folgenden Beispiel wird gezeigt, wie bestimmte Eigenschaften abgefragt werden.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Allerdings werden alle Eigenschaften eines eingebetteten Objekts zurückgegeben, auch wenn die Abfrage eingebettete Objekteigenschaften angibt.

Das folgende Beispiel zeigt zwei Abfragen, die dieselben Daten zurückgeben.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Wenn eine System Eigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält Sie **null**. Beispielsweise ist der Wert der **\_ \_ RelPath** -System Eigenschaft für alle Ereignis Abfragen **null** .

Die folgenden Systemeigenschaften enthalten **null** für Ereignis Abfragen:

<dl> \_\_Namespace  
\_\_ADS  
\_\_RelPath  
\_\_Servers  
</dl>

Weitere Informationen finden Sie unter [WMI-System Eigenschafts Referenz](wmi-system-properties.md).

Alle Ereignis Abfragen können eine optionale [WHERE-Klausel](where-clause.md)enthalten, aber WHERE-Klauseln werden hauptsächlich von Consumern verwendet, um zusätzliche Filter anzugeben. Es wird dringend empfohlen, dass Consumer immer eine WHERE-Klausel angeben. Die Kosten einer komplexen Abfrage sind im Vergleich zu den Kosten für die Bereitstellung und Verarbeitung nicht benötigter Benachrichtigungen minimal.

Das folgende Beispiel zeigt eine Abfrage, die Benachrichtigungen zu allen instanzänderungsereignissen anfordert, die die hypothetische Klasse **EmailEvent** betreffen.


```sql
SELECT * FROM EmailEvent
```



Wenn Ereignisse, die **EmailEvent** zugeordnet sind, häufig auftreten, wird der Consumer mit Ereignissen überflutet. Eine bessere Abfrage fordert Ereignisse nur dann an, wenn bestimmte Bedingungen Eigenschaften der angegebenen Klasse verwenden, z. b. wenn die Wichtigkeits Stufe hoch ist.

Das folgende Beispiel zeigt die Abfrage, die Sie verwenden können, wenn **emailimportance** eine Eigenschaft der Klasse **EmailEvent** ist.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Beachten Sie, dass WMI eine Abfrage aus verschiedenen Gründen ablehnen kann. Beispielsweise kann die Abfrage zu komplex oder für die Auswertung ressourcenintensiv sein. In diesem Fall gibt WMI bestimmte Fehlercodes zurück, z. **b. \_ eine \_ ungültige \_ WBEM E-Abfrage**.

Eigenschaften von eingebetteten Objekten können in der WHERE-Klausel verwendet werden.

Im folgenden Beispiel wird gezeigt, wie Objekte abgefragt werden, bei denen die **TargetInstance** -Eigenschaft der System Klasse [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) ein eingebettetes [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Objekt und **FreeSpace** eine Eigenschaft von **Win32 \_ LogicalDisk** ist.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Beispiele

Das [Überwachungs Erstellungs Ereignis für einen bestimmten Prozessnamen](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript-Beispiel auf TechNet verwendet die SELECT-Anweisung zum Überwachen von WMI-Instanzen Erstellungs Ereignissen für den Win32- \_ Prozess, Filtern nach einem bestimmten Prozessnamen.

 

 
