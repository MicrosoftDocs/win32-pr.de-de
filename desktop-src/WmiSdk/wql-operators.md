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
# <a name="wql-operators"></a><span data-ttu-id="84660-103">WQL-Operatoren</span><span class="sxs-lookup"><span data-stu-id="84660-103">WQL Operators</span></span>

<span data-ttu-id="84660-104">Die Windows-Verwaltungsinstrumentation Query Language (WQL) unterstützt wie folgt eine Reihe von Standard Operatoren, die in der [WHERE-Klausel](where-clause.md) einer SELECT-Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84660-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="84660-105">Operator</span><span class="sxs-lookup"><span data-stu-id="84660-105">Operator</span></span>       | <span data-ttu-id="84660-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84660-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="84660-107">Gleich</span><span class="sxs-lookup"><span data-stu-id="84660-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="84660-108">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="84660-108">Less than</span></span>                |
| >           | <span data-ttu-id="84660-109">Größer als</span><span class="sxs-lookup"><span data-stu-id="84660-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="84660-110">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="84660-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="84660-111">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="84660-111">Greater than or equal to</span></span> |
| <span data-ttu-id="84660-112">! = oder <></span><span class="sxs-lookup"><span data-stu-id="84660-112">!= or <></span></span> | <span data-ttu-id="84660-113">Ungleich</span><span class="sxs-lookup"><span data-stu-id="84660-113">Not equal to</span></span>             |



 

<span data-ttu-id="84660-114">Es gibt einige zusätzliche WQL-spezifische Operatoren: ist, ist nicht, ISA und like.</span><span class="sxs-lookup"><span data-stu-id="84660-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="84660-115">Die Operatoren is und is not sind in der WHERE-Klausel nur gültig, wenn die Konstante **null** ist.</span><span class="sxs-lookup"><span data-stu-id="84660-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="84660-116">Die folgenden Abfragen sind z. b. gültig:</span><span class="sxs-lookup"><span data-stu-id="84660-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="84660-117">Die folgenden Abfragen zeigen die ungültige Verwendung von is an und ist nicht:</span><span class="sxs-lookup"><span data-stu-id="84660-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="84660-118">Der ISA-Operator wird in der WHERE-Klausel von Daten-und Ereignis Abfragen verwendet, um eingebettete Objekte für eine Klassenhierarchie zu testen.</span><span class="sxs-lookup"><span data-stu-id="84660-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="84660-119">Der ISA-Operator entfällt, dass neu abgeleitete Klassen nachverfolgt werden müssen, wenn eine Hierarchie von Klassen angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="84660-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="84660-120">Wenn Sie ISA verwenden, werden neu erstellte und vorhandene Unterklassen der angeforderten Klasse automatisch im Resultset eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="84660-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="84660-121">Weitere Informationen zur Syntax und Verwendung dieses Operators finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="84660-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="84660-122">ISA-Operator für Daten Abfragen</span><span class="sxs-lookup"><span data-stu-id="84660-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="84660-123">ISA-Operator für Ereignis Abfragen</span><span class="sxs-lookup"><span data-stu-id="84660-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="84660-124">ISA-Operator für Schema Abfragen</span><span class="sxs-lookup"><span data-stu-id="84660-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="84660-125">Der Like-Operator ist in der WHERE-Klausel gültig und wird verwendet, um zu bestimmen, ob eine bestimmte Zeichenfolge mit einem angegebenen Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="84660-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="84660-126">Die folgende Abfrage gibt z. b. alle Instanzen von Win32- \_ Klassen zurück.</span><span class="sxs-lookup"><span data-stu-id="84660-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="84660-127">Weitere Informationen zur Syntax und Verwendung dieses Operators finden Sie unter like- [Operator](like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="84660-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



