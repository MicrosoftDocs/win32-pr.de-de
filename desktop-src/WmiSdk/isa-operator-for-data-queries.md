---
description: Verwenden Sie den ISA-Operator in der WHERE-Klausel einer Datenabfrage, um eingebettete Objekte in einer Klassenhierarchie anzufordern.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: ISA-Operator für Daten Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363245"
---
# <a name="isa-operator-for-data-queries"></a>ISA-Operator für Daten Abfragen

Verwenden Sie den ISA-Operator in der WHERE-Klausel einer Datenabfrage, um eingebettete Objekte in einer Klassenhierarchie anzufordern.

Das folgende Beispiel zeigt die Syntax, um eingebettete Objekte in einer Klassenhierarchie anzufordern.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



Das Ergebnis umfasst Instanzen der- **Klasse** mit eingebetteten Objekten, **die von "** " in der Eigenschaft " **embeddedprop** " aus "" abgeleitet werden. Nicht jede Instanz des **Class** -Objekts wird von der- **Klasse** abgeleitet. das Ergebnis gibt jedoch die eingebetteten Objekte zurück, die von der- **Klasse** abgeleitet werden.

In der folgenden Abfrage enthält **ClassA** z. b. die schwach typisierte **embeddebug** -Eigenschaft. Die **ClassA** -Klasse verfügt über zehn Instanzen. Fünf dieser Instanzen verfügen über eingebettete Objekte mit einem Typ, der von **classz** abgeleitet ist. Die anderen fünf haben eingebettete Objekte anderer Typen.

Im folgenden Beispiel wird die Abfrage gezeigt, die die fünf Instanzen zurückgibt, die die Objekte enthalten, die von **classz** abgeleitet werden.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



