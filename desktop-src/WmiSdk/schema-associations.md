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
# <a name="schema-associations"></a><span data-ttu-id="e1dec-103">Schema Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="e1dec-103">Schema Associations</span></span>

<span data-ttu-id="e1dec-104">Schema Zuordnungs Abfragen verwenden die gleichen Anweisungen wie bei Daten Zuordnungs Abfragen: assoziatoren von und verweisen von.</span><span class="sxs-lookup"><span data-stu-id="e1dec-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="e1dec-105">Bei Daten Zuordnungs Abfragen werden jedoch Klassen Instanzen zurückgegeben, und bei Schema Zuordnungs Abfragen werden Klassennamen zurückgegeben, die an Zuordnungs Beziehungen teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="e1dec-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="e1dec-106">Verwenden Sie z. b. eine Schema Abfrage, um alle im Schema definierten Zuordnungs Klassen zu suchen, die auf eine Quell Klasse verweisen.</span><span class="sxs-lookup"><span data-stu-id="e1dec-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="e1dec-107">Die Syntax für die assoziatoren von-und-verweisen auf-Anweisungen ist für Schema Zuordnungs Abfragen identisch, da dies für Daten Assoziations Abfragen mit den folgenden Ausnahmen gilt:</span><span class="sxs-lookup"><span data-stu-id="e1dec-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="e1dec-108">Das Quell Objekt ist eine-Klasse anstelle einer-Instanz.</span><span class="sxs-lookup"><span data-stu-id="e1dec-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="e1dec-109">Es gibt ein zusätzliches Schlüsselwort, **SchemaOnly**, das die Abfrage als Anwendung auf ein Schema anstelle von Daten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e1dec-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="e1dec-110">Das **classdefsonly** -Schlüsselwort ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e1dec-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="e1dec-111">Im folgenden Beispiel wird die gesamte Syntax der ASSOCIATORS of-Anweisung für eine Schema Abfrage veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e1dec-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="e1dec-112">Ausführliche Syntax finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="e1dec-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


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



<span data-ttu-id="e1dec-113">Das folgende Beispiel zeigt eine Abfrage, die die **Protokoll** -und **Treiber** Klassen zurückgibt, die zwei Klassen, die auf die Quell Klasse verweisen.</span><span class="sxs-lookup"><span data-stu-id="e1dec-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="e1dec-114">Die folgende Abfrage gibt nur die **Driver** -Klasse zurück, weil die vom Schlüsselwort " **AssocClass** " erteilte Einschränkung eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="e1dec-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="e1dec-115">Die komplette Syntax der References of-Anweisung für eine Schema Abfrage lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e1dec-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="e1dec-116">Ausführliche Syntax finden Sie unter [References of-Anweisung](references-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="e1dec-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="e1dec-117">Schema Zuordnungs Abfragen geben möglicherweise doppelte Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="e1dec-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="e1dec-118">Beispielsweise gibt die folgende Abfrage beim Auflisten von Klassen im **root \\ CIMV2** -Namespace mehrmals die Klasse [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) zurück.</span><span class="sxs-lookup"><span data-stu-id="e1dec-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
