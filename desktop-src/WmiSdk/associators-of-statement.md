---
description: Ruft alle-Instanzen ab, die einer bestimmten Quell Instanz zugeordnet sind.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: Assoziatoren der Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347638"
---
# <a name="associators-of-statement"></a><span data-ttu-id="09975-103">Assoziatoren der Anweisung</span><span class="sxs-lookup"><span data-stu-id="09975-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="09975-104">Die ASSOCIATORS of-Anweisung ruft alle-Instanzen ab, die einer bestimmten Quell Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="09975-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="09975-105">Die abgerufenen Instanzen werden als Endpunkte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="09975-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="09975-106">Jeder Endpunkt wird so oft zurückgegeben, wie es Zuordnungen zwischen ihm und dem Quell Objekt gibt.</span><span class="sxs-lookup"><span data-stu-id="09975-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="09975-107">Nehmen wir beispielsweise an, dass die Instanzen a, B, X und Y vorhanden sind. Es sind zwei Assoziations Instanzen vorhanden: eine, die a und X verknüpft, und eine andere, die B und Y verknüpft. Die folgende Abfrage gibt den einzelnen Endpunkt X zurück:</span><span class="sxs-lookup"><span data-stu-id="09975-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="09975-108">Wenn jedoch eine weitere Zuordnung vorhanden ist, die A und X verknüpft, gibt die obige Abfrage zwei X-Endpunkte zurück.</span><span class="sxs-lookup"><span data-stu-id="09975-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="09975-109">Die grundlegende Syntax für die assoziatoren der-Anweisung lautet:</span><span class="sxs-lookup"><span data-stu-id="09975-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="09975-110">Beachten Sie, dass die geschweiften Klammern Teil der Syntax sind.</span><span class="sxs-lookup"><span data-stu-id="09975-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="09975-111">Ein gültiger Objekt Pfad kann für objectPath verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09975-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="09975-112">Die Token im Objekt Pfad dürfen keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="09975-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="09975-113">Beispielsweise gibt die Abfrage in der folgenden Liste-Instanzen zurück, die dem angegebenen logischen Datenträger zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="09975-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="09975-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="09975-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="09975-116">Wie bei der [SELECT-Anweisung](select-statement-for-data-queries.md)können auch assoziatoren der-Anweisung eine [WHERE-Klausel](where-clause.md)enthalten, aber die WHERE-Klausel für einen assoziators der-Anweisung unterscheidet sich stark von der SELECT-Klausel der-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="09975-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="09975-117">Die [WHERE-Klausel](where-clause.md) der ASSOCIATORS of-Anweisung kann ein oder mehrere der folgenden vordefinierten Schlüsselwörter und ihre Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="09975-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



<span data-ttu-id="09975-118">Beachten Sie, dass die optionalen Unterklauseln nicht durch Kommas voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="09975-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="09975-119">Das Schlüsselwort " **AssocClass** " gibt an, dass die zurückgegebenen Endpunkte über die angegebene Klasse oder eine der abgeleiteten Klassen mit der Quelle verknüpft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="09975-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="09975-120">Die Abfrage in der folgenden Liste gibt z. b. nur Endpunkte zurück, die der Quelle über die [**Win32 \_ systemdevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) -Zuordnungs Klasse oder eine der abgeleiteten Klassen zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="09975-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="09975-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="09975-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="09975-123">Das **classdefsonly** -Schlüsselwort gibt an, dass die-Klausel ein Resultset von Klassen Definitions Objekten anstelle tatsächlicher Instanzen der Klassen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="09975-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="09975-124">Bei diesen Objekten handelt es sich um die Definitionen von Klassen, zu denen die Endpunkt Instanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="09975-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="09975-125">Die Abfrage in der folgenden Liste gibt beispielsweise Definitionen für das [**Win32- \_ Verzeichnis**](/windows/desktop/CIMWin32Prov/win32-directory) und die [**Win32- \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) -Klassen zurück:</span><span class="sxs-lookup"><span data-stu-id="09975-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="09975-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="09975-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="09975-128">Die Schlüsselwörter **classdefsonly** und **resultClass** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="09975-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="09975-129">Die gemeinsame Verwendung verursacht einen ungültigen Abfrage Fehler.</span><span class="sxs-lookup"><span data-stu-id="09975-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="09975-130">Das "Requirements **dassocqualifier** "-Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte dem Quell Objekt über eine Association-Klasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="09975-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="09975-131">Dieser Filtertyp wird verwendet, um große Bereiche von Endpunkten auszuschließen, es sei denn, die Endpunkte werden dem Ziel über einen bestimmten Satz von markierten Zuordnungs Klassen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="09975-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="09975-132">Die Abfrage in der folgenden Liste gibt beispielsweise Endpunkt Instanzen zurück, wenn die Association-Klasse einen Qualifizierer namens **Association** enthält.</span><span class="sxs-lookup"><span data-stu-id="09975-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="09975-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="09975-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="09975-135">Das "Requirements **dqualifier** "-Schlüsselwort gibt an, dass die dem Quell Objekt zugeordneten zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen</span><span class="sxs-lookup"><span data-stu-id="09975-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="09975-136">Das "Requirements **dqualifier** "-Schlüsselwort kann verwendet werden, um bestimmte Typen von Instanzen in das Resultset einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="09975-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="09975-137">Die Abfrage in der folgenden Liste gibt beispielsweise Endpunkt Instanzen zurück, die einen Qualifizierer namens [**locale**](swbemobjectpath-locale.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="09975-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="09975-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="09975-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="09975-140">Das **resultClass** -Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte, die dem Quell Objekt zugeordnet sind, zu der angegebenen Klasse gehören bzw. davon abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="09975-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="09975-141">Die Abfrage in der folgenden Liste gibt beispielsweise Endpunkt Instanzen zurück, die von der [**CIM- \_ Verzeichnis**](/windows/desktop/CIMWin32Prov/cim-directory) Klasse abgeleitet sind:</span><span class="sxs-lookup"><span data-stu-id="09975-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="09975-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="09975-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="09975-144">Die Schlüsselwörter **classdefsonly** und **resultClass** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="09975-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="09975-145">Die gemeinsame Verwendung verursacht einen ungültigen Abfrage Fehler.</span><span class="sxs-lookup"><span data-stu-id="09975-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="09975-146">Das **RESULTROLE** -Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="09975-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="09975-147">Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweis Eigenschaft vom Typ [ref](references.md). Beispielsweise kann das **RESULTROLE** -Schlüsselwort verwendet werden, um alle Endpunkte abzurufen, die die **GroupComponent** -Eigenschaft in ihrer Zuordnung zu einem Quell Objekt aufweisen, wie die folgende Abfrage veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="09975-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="09975-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="09975-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="09975-150">Das **Role** -Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt beteiligt sind, in dem das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="09975-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="09975-151">Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweis Eigenschaft vom Typ **ref**. Beispielsweise kann das **Role** -Schlüsselwort verwendet werden, um alle Endpunkte abzurufen, die einem Quell Objekt zugeordnet sind, das die **GroupComponent** -Eigenschaft hat, wie die folgende Abfrage veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="09975-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="09975-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such</span><span class="sxs-lookup"><span data-stu-id="09975-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="09975-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen</span><span class="sxs-lookup"><span data-stu-id="09975-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="09975-154">Komplexe Abfragen können nicht "and" oder "or" verwenden, um Schlüsselwörter für assoziatoren von und [verweisen](references-of-statement.md) auf-Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="09975-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="09975-155">Außerdem ist das Gleichheitszeichen der einzige gültige Operator, der in solchen Abfragen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="09975-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="09975-156">Beispielsweise ist die folgende Abfrage gültig:</span><span class="sxs-lookup"><span data-stu-id="09975-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="09975-157">Die folgenden Beispiele sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="09975-157">The next examples are not valid.</span></span> <span data-ttu-id="09975-158">Im ersten Beispiel wird nicht das Gleichheitszeichen verwendet, und das zweite Beispiel versucht fälschlicherweise, das **-** Schlüsselwort und das-Schlüsselwort zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="09975-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
