---
description: Beschreibt WQL-Operatoren, die in der WHERE-Klausel oder der SELECT-Anweisung verwendet werden.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: WQL-Operatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a441afb661e4f8d92e21d944462dddd6d7390fd2dbe871512342f7c9251d6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553087"
---
# <a name="wql-operators"></a>WQL-Operatoren

Die Windows Management Instrumentation Query Language (WQL) unterstützt eine Reihe von Standardoperatoren, die in der [WHERE-Klausel](where-clause.md) einer SELECT-Anweisung wie folgt verwendet werden.



| Operator       | BESCHREIBUNG              |
|----------------|--------------------------|
| =              | Gleich                 |
| <           | Kleiner als                |
| >           | Größer als             |
| <=          | Kleiner als oder gleich    |
| >=          | Größer als oder gleich |
| != oder <> | Ungleich             |



 

Es gibt einige zusätzliche WQL-spezifische Operatoren: IS, IS NOT, ISA und LIKE. Die Operatoren IS und IS NOT sind in der WHERE-Klausel nur gültig, wenn die Konstante **NULL ist.** Beispielsweise sind die folgenden Abfragen gültig:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Die folgenden Abfragen zeigen ungültige Verwendungen von IS und IS NOT:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



Der ISA-Operator wird in der WHERE-Klausel von Daten- und Ereignisabfragen verwendet, um eingebettete Objekte für eine Klassenhierarchie zu testen. Der ISA-Operator macht es nicht mehr notwendig, neu abgeleitete Klassen beim Anfordern einer Klassenhierarchie nachverfolgung zu lassen. Wenn Sie ISA verwenden, werden neu erstellte und vorhandene Unterklassen der angeforderten Klasse automatisch in das Ergebnisset aufgenommen.

Weitere Informationen zur Syntax und Verwendung dieses Operators finden Sie in den folgenden Themen:

-   [ISA-Operator für Datenabfragen](isa-operator-for-data-queries.md)
-   [ISA-Operator für Ereignisabfragen](isa-operator-for-event-queries.md)
-   [ISA-Operator für Schemaabfragen](isa-operator-for-schema-queries.md)

Der LIKE-Operator ist in der WHERE-Klausel gültig und wird verwendet, um zu bestimmen, ob eine bestimmte Zeichenfolge einem angegebenen Muster entspricht. Die folgende Abfrage gibt beispielsweise alle Instanzen von Win32-Klassen \_ zurück.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Weitere Informationen zur Syntax und Verwendung dieses Operators finden Sie unter [LIKE-Operator](like-operator.md).

 

 



