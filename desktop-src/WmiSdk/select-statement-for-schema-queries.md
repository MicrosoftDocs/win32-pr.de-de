---
description: Schema Daten Abfragen verwenden die SELECT-Anweisung mit einer ähnlichen Syntax wie bei Daten Abfragen.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: SELECT-Anweisung für Schema Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217954"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="5e8d6-103">SELECT-Anweisung für Schema Abfragen</span><span class="sxs-lookup"><span data-stu-id="5e8d6-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="5e8d6-104">Schema Daten Abfragen verwenden die SELECT-Anweisung mit einer ähnlichen Syntax wie bei [Daten Abfragen](select-statement-for-data-queries.md).</span><span class="sxs-lookup"><span data-stu-id="5e8d6-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="5e8d6-105">Der Unterschied besteht in der Verwendung einer speziellen Klasse mit dem Namen "Meta \_ Class", die die Abfrage als Schema Abfrage bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="5e8d6-106">Im folgenden Beispiel werden alle Klassendefinitionen angefordert, die sich innerhalb des aktuellen Namespace befinden.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="5e8d6-107">Schema Abfragen unterstützen nur " \* ".</span><span class="sxs-lookup"><span data-stu-id="5e8d6-107">Schema queries only support "\*".</span></span> <span data-ttu-id="5e8d6-108">Um den Gültigkeitsbereich der zurückgegebenen Definitionen einzuschränken, kann ein Anbieter eine WHERE-Klausel hinzufügen, die eine bestimmte Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="5e8d6-109">Im folgenden Beispiel wird gezeigt, wie eine WHERE-Klausel hinzugefügt wird, um eine bestimmte Klasse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="5e8d6-110">Die spezielle Eigenschaft, die **\_ \_ als bezeichnet wird, identifiziert die** Zielklasse für eine Schema Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="5e8d6-111">Beachten Sie, dass der ISA-Operator mit der **\_ \_ this** -Eigenschaft verwendet werden muss, um Definitionen für die Unterklassen der Zielklasse anzufordern.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="5e8d6-112">Die vorherige Abfrage gibt die Definition für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse und Definitionen für alle zugehörigen Unterklassen zurück.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="5e8d6-113">Im folgenden Beispiel wird gezeigt, wie eine Klassendefinition für eine einzelne Klasse mithilfe der- **\_ \_ Klassen** System Eigenschaft angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="5e8d6-114">Diese Abfrage entspricht dem Aufrufen der [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode oder der [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode, wobei der Objekt Pfad Parameter auf "Win32 \_ LogicalDisk" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="5e8d6-115">Das folgende VBScript-Codebeispiel ruft alle untergeordneten Klassen einer WMI-Klasse der obersten Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="5e8d6-116">Die \_ \_ WMI-System Eigenschaft der Dynastie enthält den Namen der Klasse der obersten Ebene, von der eine Klasse abgeleitet wird, mit der Sie alle Klassen in einem Namespace abrufen können, die von einer Klasse der obersten Ebene abgeleitet werden, einschließlich dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="5e8d6-117">Das folgende VBScript Ruft eine unmittelbare untergeordnete Klasse für eine WMI-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="5e8d6-118">Das folgende VBScript Ruft die Klassen der obersten Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="5e8d6-119">Für alle Klassen der obersten Ebene in einem WMI-Namespace \_ \_ ist die System Eigenschaft "Superclass" NULL.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="5e8d6-120">Daher ist es möglich, die Klassen der obersten Ebene abzurufen, indem Sie nach einer NULL-Superclass suchen.</span><span class="sxs-lookup"><span data-stu-id="5e8d6-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
