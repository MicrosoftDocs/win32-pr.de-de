---
description: Beschreibt WQL-Operatoren, die in der WHERE-Klausel oder SELECT-Anweisung verwendet werden.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: WQL-Operatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362276"
---
# <a name="wql-operators"></a>WQL-Operatoren

Die Windows-Verwaltungsinstrumentation Query Language (WQL) unterstützt wie folgt eine Reihe von Standard Operatoren, die in der [WHERE-Klausel](where-clause.md) einer SELECT-Anweisung verwendet werden.



| Operator       | BESCHREIBUNG              |
|----------------|--------------------------|
| =              | Gleich                 |
| <           | Kleiner als                |
| >           | Größer als             |
| <=          | Kleiner als oder gleich    |
| >=          | Größer als oder gleich |
| ! = oder <> | Ungleich             |



 

Es gibt einige zusätzliche WQL-spezifische Operatoren: ist, ist nicht, ISA und like. Die Operatoren is und is not sind in der WHERE-Klausel nur gültig, wenn die Konstante **null** ist. Die folgenden Abfragen sind z. b. gültig:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Die folgenden Abfragen zeigen die ungültige Verwendung von is an und ist nicht:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



Der ISA-Operator wird in der WHERE-Klausel von Daten-und Ereignis Abfragen verwendet, um eingebettete Objekte für eine Klassenhierarchie zu testen. Der ISA-Operator entfällt, dass neu abgeleitete Klassen nachverfolgt werden müssen, wenn eine Hierarchie von Klassen angefordert wird. Wenn Sie ISA verwenden, werden neu erstellte und vorhandene Unterklassen der angeforderten Klasse automatisch im Resultset eingeschlossen.

Weitere Informationen zur Syntax und Verwendung dieses Operators finden Sie in den folgenden Themen:

-   [ISA-Operator für Daten Abfragen](isa-operator-for-data-queries.md)
-   [ISA-Operator für Ereignis Abfragen](isa-operator-for-event-queries.md)
-   [ISA-Operator für Schema Abfragen](isa-operator-for-schema-queries.md)

Der Like-Operator ist in der WHERE-Klausel gültig und wird verwendet, um zu bestimmen, ob eine bestimmte Zeichenfolge mit einem angegebenen Muster übereinstimmt. Die folgende Abfrage gibt z. b. alle Instanzen von Win32- \_ Klassen zurück.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Weitere Informationen zur Syntax und Verwendung dieses Operators finden Sie unter like- [Operator](like-operator.md).

 

 



