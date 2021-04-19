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
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="386d5-103">ISA-Operator für Daten Abfragen</span><span class="sxs-lookup"><span data-stu-id="386d5-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="386d5-104">Verwenden Sie den ISA-Operator in der WHERE-Klausel einer Datenabfrage, um eingebettete Objekte in einer Klassenhierarchie anzufordern.</span><span class="sxs-lookup"><span data-stu-id="386d5-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="386d5-105">Das folgende Beispiel zeigt die Syntax, um eingebettete Objekte in einer Klassenhierarchie anzufordern.</span><span class="sxs-lookup"><span data-stu-id="386d5-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="386d5-106">Das Ergebnis umfasst Instanzen der- **Klasse** mit eingebetteten Objekten, **die von "** " in der Eigenschaft " **embeddedprop** " aus "" abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="386d5-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="386d5-107">Nicht jede Instanz des **Class** -Objekts wird von der- **Klasse** abgeleitet. das Ergebnis gibt jedoch die eingebetteten Objekte zurück, die von der- **Klasse** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="386d5-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="386d5-108">In der folgenden Abfrage enthält **ClassA** z. b. die schwach typisierte **embeddebug** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="386d5-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="386d5-109">Die **ClassA** -Klasse verfügt über zehn Instanzen.</span><span class="sxs-lookup"><span data-stu-id="386d5-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="386d5-110">Fünf dieser Instanzen verfügen über eingebettete Objekte mit einem Typ, der von **classz** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="386d5-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="386d5-111">Die anderen fünf haben eingebettete Objekte anderer Typen.</span><span class="sxs-lookup"><span data-stu-id="386d5-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="386d5-112">Im folgenden Beispiel wird die Abfrage gezeigt, die die fünf Instanzen zurückgibt, die die Objekte enthalten, die von **classz** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="386d5-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



