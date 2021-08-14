---
description: Verwenden Sie den ISA-Operator in der WHERE-Klausel einer Datenabfrage, um eingebettete Objekte in einer Klassenhierarchie anzufordern.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: ISA-Operator für Datenabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33c0bc4b78101a4b1e6a38997518fec543b9eb49e42b28cbb2500c321f56ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318302"
---
# <a name="isa-operator-for-data-queries"></a>ISA-Operator für Datenabfragen

Verwenden Sie den ISA-Operator in der WHERE-Klausel einer Datenabfrage, um eingebettete Objekte in einer Klassenhierarchie anzufordern.

Das folgende Beispiel zeigt die Syntax zum Anfordern eingebetteter Objekte in einer Klassenhierarchie.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



Das Ergebnis umfasst Instanzen der **-Klasse** mit eingebetteten Objekten, die von **ParentClass** in der **EmbeddedProp-Eigenschaft** abgeleitet sind. Nicht jede Instanz des **Class-Objekts** wird von **ParentClass** abgeleitet, aber das Ergebnis gibt die eingebetteten Objekte zurück, die von **ParentClass** abgeleitet werden.

In der folgenden Abfrage enthält **ClassA** beispielsweise die schwach typisierte **EmbeddedObj-Eigenschaft.** Die **ClassA-Klasse** verfügt über zehn Instanzen. Fünf dieser Instanzen verfügen über eingebettete Objekte mit einem von **ClassZ** abgeleiteten Typ. Die anderen fünf verfügen über eingebettete Objekte anderer Typen.

Das folgende Beispiel zeigt die Abfrage, die die fünf Instanzen zurückgibt, die die von **ClassZ** abgeleiteten Objekte enthalten.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



