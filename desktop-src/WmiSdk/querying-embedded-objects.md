---
description: Es gibt mehrere Möglichkeiten, wie eine Abfrage eine Abfrage durchführt, wenn eine Ereignisklasse abgefragt wird, die eingebettete Objekte enthält. Die von der Abfrage zurückgegebenen Ergebnisse variieren abhängig von der Form der Abfrage, die Sie verwenden.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Abfragen von eingebetteten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755056"
---
# <a name="querying-embedded-objects"></a>Abfragen von eingebetteten Objekten

Es gibt mehrere Möglichkeiten, wie eine Abfrage eine Abfrage durchführt, wenn eine Ereignisklasse abgefragt wird, die eingebettete Objekte enthält. Die von der Abfrage zurückgegebenen Ergebnisse variieren abhängig von der Form der Abfrage, die Sie verwenden.

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

Die folgende Abfrage gibt sowohl die eingebetteten Klassen **E1** als auch **E2** zurück, die jeweils **Eigenschaft PROP1** und **Prop2** mit Daten aufgefüllt haben.

`SELECT * FROM MyEvent`

Die folgende Abfrage gibt das **E1** Embedded-Objekt zurück, wobei jedoch weder **Eigenschaft PROP1** noch **Prop2** mit Daten aufgefüllt wird.

`SELECT E1 FROM MyEvent`

Die folgende Abfrage gibt die eingebettete Klasse **E1** zurück, wobei nur **Eigenschaft PROP1** mit Daten aufgefüllt wird.

`SELECT E1.Prop1 FROM MyEvent`

Die folgende Abfrage gibt sowohl die eingebetteten Klassen **E1** als auch **E2** zurück, die jeweils **Eigenschaft PROP1** und **Prop2** mit Daten aufgefüllt haben.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Dies entspricht der ersten Abfrage mit dem Sternchen ( \* ) anstelle der Angabe der einzelnen Objekte und Eigenschaften.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abfragen mit WQL](querying-with-wql.md)
</dt> </dl>

 

 



