---
description: Die References of-Anweisung ruft alle Assoziations Instanzen ab, die auf eine bestimmte Quell Instanz verweisen.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: Verweise der Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350569"
---
# <a name="references-of-statement"></a><span data-ttu-id="9916f-103">Verweise der Anweisung</span><span class="sxs-lookup"><span data-stu-id="9916f-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="9916f-104">Die References of-Anweisung ruft alle Assoziations Instanzen ab, die auf eine bestimmte Quell Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="9916f-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="9916f-105">Die References of-Anweisung ähnelt den assoziatoren der-Anweisung in der-Syntax.</span><span class="sxs-lookup"><span data-stu-id="9916f-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="9916f-106">Anstatt Endpunkt Instanzen abzurufen, ruft Sie jedoch die dazwischen liegenden Zuordnungs Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="9916f-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="9916f-107">Die Verweise der WHERE-Klausel können ein oder mehrere der folgenden vordefinierten Schlüsselwörter und ihre Werte einschließen:</span><span class="sxs-lookup"><span data-stu-id="9916f-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="9916f-108">Um ein Quell Objekt anzugeben, verwenden Sie einen beliebigen gültigen Objekt Pfad für SourceObject.</span><span class="sxs-lookup"><span data-stu-id="9916f-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="9916f-109">Wie bei der SELECT-Anweisung ist die WHERE-Klausel optional und wird verwendet, um die Abfrage weiter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9916f-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="9916f-110">Das heißt, dass die folgende Anweisung vollständig gültig ist:</span><span class="sxs-lookup"><span data-stu-id="9916f-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="9916f-111">Das **classdefsonly** -Schlüsselwort gibt an, dass die Anweisung ein Resultset von Klassen Definitions Objekten anstelle tatsächlicher Instanzen der Zuordnungs Klassen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9916f-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="9916f-112">Diese Objekte enthalten Definitionen von Klassen, zu denen die Instanzen, die auf das Quell Objekt verweisen, gehören.</span><span class="sxs-lookup"><span data-stu-id="9916f-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="9916f-113">Die folgende Anweisung gibt beispielsweise Definitionen für die **adapterdriver** -Klasse und die **adapterprotocol** -Klasse zurück:</span><span class="sxs-lookup"><span data-stu-id="9916f-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="9916f-114">Das Requirements **dqualifier** -Schlüsselwort gibt an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen</span><span class="sxs-lookup"><span data-stu-id="9916f-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="9916f-115">Das "Requirements **dqualifier** "-Schlüsselwort kann verwendet werden, um bestimmte Instanzen von Zuordnungen in das Resultset einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="9916f-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="9916f-116">Die folgende Anweisung gibt beispielsweise Association-Instanzen zurück, die einen Qualifizierer namens **adaptertag** enthalten:</span><span class="sxs-lookup"><span data-stu-id="9916f-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="9916f-117">Das **resultClass** -Schlüsselwort gibt an, dass die zurückgegebenen Zuordnungs Objekte zu oder von der angegebenen Klasse abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9916f-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="9916f-118">Beispielsweise gibt die folgende Anweisung Zuordnungen der **adapterdriver** -Klasse oder Unterklassen von **adapterdriver** zurück:</span><span class="sxs-lookup"><span data-stu-id="9916f-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="9916f-119">Die Schlüsselwörter **classdefsonly** und **resultClass** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="9916f-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="9916f-120">Die gemeinsame Verwendung verursacht einen ungültigen Abfrage Fehler.</span><span class="sxs-lookup"><span data-stu-id="9916f-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="9916f-121">Das **Role** -Schlüsselwort gibt an, dass die zurückgegebenen Zuordnungen nur solche sind, in denen das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="9916f-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="9916f-122">Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweis Eigenschaft vom Typ [ref](references.md). Das **Role** -Schlüsselwort ist hilfreich bei Zuordnungen, bei denen ein bestimmtes Objekt in einigen Fällen eine Rolle spielen kann, und eine andere Rolle in anderen, z. b. in hierarchischen Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="9916f-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="9916f-123">Das **Role** -Schlüsselwort kann verwendet werden, um alle Zuordnungen abzurufen, in denen das Quell Objekt z. b. die Rolle des übergeordneten Elements übernimmt.</span><span class="sxs-lookup"><span data-stu-id="9916f-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="9916f-124">Die folgende Anweisung veranschaulicht die Syntax zum Abrufen von Zuordnungen, die über eine über **geordnete** Eigenschaft verfügen, die auf das Quell Objekt als übergeordnetes Element verweist:</span><span class="sxs-lookup"><span data-stu-id="9916f-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="9916f-125">Komplexe Abfragen können nicht "and" oder "or" verwenden, um Schlüsselwörter für assoziatoren von und verweisen auf-Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="9916f-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="9916f-126">Außerdem ist das Gleichheitszeichen der einzige gültige Operator, der mit den Schlüsselwörtern in diesen Abfragen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9916f-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="9916f-127">Beispielsweise ist die folgende Abfrage gültig:</span><span class="sxs-lookup"><span data-stu-id="9916f-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="9916f-128">Die folgenden Beispiele sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="9916f-128">The next examples are not valid.</span></span> <span data-ttu-id="9916f-129">Im ersten Beispiel wird nicht das Gleichheitszeichen verwendet, und das zweite Beispiel versucht fälschlicherweise, das **-** Schlüsselwort und das-Schlüsselwort zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="9916f-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



