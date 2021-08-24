---
description: Beim Abfragen einer Ereignisklasse, die eingebettete Objekte enthält, stehen Ihnen mehrere Optionen für die Form zur Verfügung, die eine Abfrage annimmt. Die von der Abfrage zurückgegebenen Ergebnisse variieren abhängig von der Form der abfrage, die Sie verwenden.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Abfragen eingebetteter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af6e0933ae12bb5867ff2ad446928d1b55f5ee7c2022ec60f53de61a3bd4bb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130912"
---
# <a name="querying-embedded-objects"></a>Abfragen eingebetteter Objekte

Beim Abfragen einer Ereignisklasse, die eingebettete Objekte enthält, stehen Ihnen mehrere Optionen für die Form zur Verfügung, die eine Abfrage annimmt. Die von der Abfrage zurückgegebenen Ergebnisse variieren abhängig von der Form der abfrage, die Sie verwenden.

## <a name="class-definitions"></a>Klassendefinitionen

Das folgende Beispiel zeigt die Klassendefinitionen, die für die WQL-Abfragen in diesem Thema verwendet werden.

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a>Beispiele

Die folgende Abfrage gibt die eingebetteten Klassen **E1** und **E2** zurück, wobei **Prop1** und **Prop2** jeweils mit Daten aufgefüllt sind.

`SELECT * FROM MyEvent`

Die folgende Abfrage gibt das eingebettete **E1-Objekt** zurück, jedoch weder **Prop1** noch **Prop2** mit Daten aufgefüllt.

`SELECT E1 FROM MyEvent`

Die folgende Abfrage gibt die eingebettete Klasse **E1** zurück, wobei nur **Prop1** mit Daten aufgefüllt ist.

`SELECT E1.Prop1 FROM MyEvent`

Die folgende Abfrage gibt die eingebetteten Klassen **E1** und **E2** zurück, wobei **Prop1** und **Prop2** jeweils mit Daten aufgefüllt sind.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Dies entspricht der ersten Abfrage, die das Sternchen ( \* ) verwendet, anstatt jedes Objekt und jede Eigenschaft anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abfragen mit WQL](querying-with-wql.md)
</dt> </dl>

 

 



