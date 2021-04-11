---
description: 'Schema Zuordnungs Abfragen verwenden die gleichen Anweisungen wie bei Daten Zuordnungs Abfragen: assoziatoren von und verweisen von.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Schema Zuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217955"
---
# <a name="schema-associations"></a>Schema Zuordnungen

Schema Zuordnungs Abfragen verwenden die gleichen Anweisungen wie bei Daten Zuordnungs Abfragen: assoziatoren von und verweisen von. Bei Daten Zuordnungs Abfragen werden jedoch Klassen Instanzen zurückgegeben, und bei Schema Zuordnungs Abfragen werden Klassennamen zurückgegeben, die an Zuordnungs Beziehungen teilnehmen können. Verwenden Sie z. b. eine Schema Abfrage, um alle im Schema definierten Zuordnungs Klassen zu suchen, die auf eine Quell Klasse verweisen.

Die Syntax für die assoziatoren von-und-verweisen auf-Anweisungen ist für Schema Zuordnungs Abfragen identisch, da dies für Daten Assoziations Abfragen mit den folgenden Ausnahmen gilt:

-   Das Quell Objekt ist eine-Klasse anstelle einer-Instanz.
-   Es gibt ein zusätzliches Schlüsselwort, **SchemaOnly**, das die Abfrage als Anwendung auf ein Schema anstelle von Daten identifiziert.
-   Das **classdefsonly** -Schlüsselwort ist ungültig.

Im folgenden Beispiel wird die gesamte Syntax der ASSOCIATORS of-Anweisung für eine Schema Abfrage veranschaulicht. Ausführliche Syntax finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



Das folgende Beispiel zeigt eine Abfrage, die die **Protokoll** -und **Treiber** Klassen zurückgibt, die zwei Klassen, die auf die Quell Klasse verweisen.


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



Die folgende Abfrage gibt nur die **Driver** -Klasse zurück, weil die vom Schlüsselwort " **AssocClass** " erteilte Einschränkung eingeschränkt ist.


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



Die komplette Syntax der References of-Anweisung für eine Schema Abfrage lautet wie folgt. Ausführliche Syntax finden Sie unter [References of-Anweisung](references-of-statement.md).


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> Schema Zuordnungs Abfragen geben möglicherweise doppelte Objekte zurück.

 

Beispielsweise gibt die folgende Abfrage beim Auflisten von Klassen im **root \\ CIMV2** -Namespace mehrmals die Klasse [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) zurück.


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
