---
description: Eine joinansichts Klasse enthält Eigenschaften aus Quell Klassen Instanzen, die durch einen allgemeinen Eigenschafts Wert verbunden sind, z. b. Class1. Eigenschaft PROP1 = Klasse2. Prop2. Jede Instanz in einer joinansichts Klasse besteht aus Teilen verschiedener Klassen Instanzen.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Erstellen einer neuen Instanz aus alten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960615"
---
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="6e921-104">Erstellen einer neuen Instanz aus alten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e921-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="6e921-105">Eine joinansichts Klasse enthält Eigenschaften aus Quell Klassen Instanzen, die durch einen allgemeinen Eigenschafts Wert verbunden sind, z. b. **Class1. Eigenschaft PROP1**  =  **Klasse2. Prop2**.</span><span class="sxs-lookup"><span data-stu-id="6e921-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="6e921-106">Jede Instanz in einer joinansichts Klasse besteht aus Teilen verschiedener Klassen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="6e921-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="6e921-107">Sie können eine Verknüpfungs Ansichts Klasse auf Ungleichheit von Eigenschafts Werten, wie z **. b. Class1. Eigenschaft PROP1**  <>  **Klasse2. Prop2** , basieren, wobei **Eigenschaft PROP1** und **Prop2** nicht derselben Eigenschaft in der Ansichts Klasse zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6e921-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="6e921-108">Eine Join-Ansichts Klasse ist hilfreich, wenn die gesuchten Informationen in separaten, aber verwandten Klassen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6e921-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="6e921-109">Wenn Sie z. b. Informationen zu einem Drucker und zur Druckerkonfiguration benötigen, können Sie eine joinansichts Klasse erstellen, die einige der Eigenschaften der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse und einige der Eigenschaften der Win32- [**Klasse \_ printerconfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) enthält.</span><span class="sxs-lookup"><span data-stu-id="6e921-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="6e921-110">Ohne den Ansichts Anbieter müssen Sie die Eigenschaften der separaten Instanzen abrufen und zusammenführen, um die benötigten Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e921-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="6e921-111">Im folgenden Verfahren wird beschrieben, wie eine joinansichts Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6e921-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="6e921-112">**So erstellen Sie eine joinansichts Klasse**</span><span class="sxs-lookup"><span data-stu-id="6e921-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="6e921-113">Beginnen Sie eine Klassendefinition mit dem [**joinon**](qualifiers-specific-to-the-view-provider.md) -Zeichen folgen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="6e921-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="6e921-114">Die Qualifizierer [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** und **Union** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="6e921-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="6e921-115">Filtern Sie ggf. die gewünschten Instanzen in der joinklasse, indem Sie den [**postjoinfilter**](postjoinfilter-qualifier.md) -Qualifizierer anwenden.</span><span class="sxs-lookup"><span data-stu-id="6e921-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="6e921-116">Mit dem [**postjoinfilter**](postjoinfilter-qualifier.md) -Anbieter können Sie die Instanzen einer Ansichts Klasse auf Instanzen beschränken, die bestimmte Bedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6e921-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="6e921-117">Erstellen Sie die Abfragen, die Quell Instanzen der Ansichts Klasse mit dem [**viewsources**](viewsources-qualifier.md) -Qualifizierer definieren.</span><span class="sxs-lookup"><span data-stu-id="6e921-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="6e921-118">Definieren Sie die Namen und Speicherorte der Namespaces, in denen sich die Quell Instanzen mit dem [**viewspaces**](viewspaces-qualifier.md) -Qualifizierer befinden.</span><span class="sxs-lookup"><span data-stu-id="6e921-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="6e921-119">Definieren Sie die gewünschten Eigenschaften in einer joinansichts Klasse mit dem [**propertysources**](propertysources-qualifier.md) -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="6e921-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="6e921-120">Wenn der joinansicht basierend auf Gleichheit Eigenschaften hinzugefügt werden, müssen die beiden Quell Eigenschaften in einem [**propertysources**](propertysources-qualifier.md) -Qualifizierer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6e921-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="6e921-121">Das folgende Codebeispiel zeigt zwei Eigenschaften, die in einem **propertysources** -Qualifizierer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6e921-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="6e921-122">Wenn Sie den [**hiddendefault-Qualifizierer**](qualifiers-specific-to-the-view-provider.md) verwenden, können Sie die Eigenschaften markieren, die zu einer Quell Klasse gehören.</span><span class="sxs-lookup"><span data-stu-id="6e921-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="6e921-123">Das folgende Codebeispiel zeigt eine Verknüpfungs Ansichts Klasse, die aus den System Monitor-Anbieter Klassen [**Win32 \_ perfrawdata \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) und dem [**Win32 \_ perfrawdata \_ perfproc- \_ Thread**](/previous-versions//aa394325(v=vs.85)) mit den Eigenschaften beider Klassen erstellt wurde, die von der **ProcessID-** Eigenschaft verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6e921-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
