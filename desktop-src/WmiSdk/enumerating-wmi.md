---
description: Enumeration ist der Vorgang, durch den eine Reihe von Objekten durchlaufen und ggf. jedes Objekt geändert wird.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Auflisten von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345871"
---
# <a name="enumerating-wmi"></a><span data-ttu-id="6a91c-103">Auflisten von WMI</span><span class="sxs-lookup"><span data-stu-id="6a91c-103">Enumerating WMI</span></span>

<span data-ttu-id="6a91c-104">Enumeration ist der Vorgang, durch den eine Reihe von Objekten durchlaufen und ggf. jedes Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6a91c-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="6a91c-105">Beispielsweise können Sie eine Reihe von [**Win32 \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) -Objekten durchlaufen, um nach einer bestimmten Seriennummer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6a91c-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="6a91c-106">Beachten Sie, dass WMI nur Objekte zurückgibt, auf die Sie über Sicherheits Zugriff verfügen, obwohl Sie jedes beliebige Objekt auflisten können.</span><span class="sxs-lookup"><span data-stu-id="6a91c-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="6a91c-107">Enumerationen von großen Datasets können eine große Menge an Ressourcen und eine Leistungssteigerung erfordern.</span><span class="sxs-lookup"><span data-stu-id="6a91c-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="6a91c-108">Weitere Informationen finden Sie unter [verbessern der enumerationsleistung](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="6a91c-109">Sie können auch Daten mit einer spezifischeren Abfrage anfordern.</span><span class="sxs-lookup"><span data-stu-id="6a91c-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="6a91c-110">Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="6a91c-111">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="6a91c-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="6a91c-112">Auflisten von WMI mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a91c-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="6a91c-113">Auflisten von WMI mit c# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="6a91c-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="6a91c-114">Auflisten von WMI mit c# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="6a91c-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="6a91c-115">Auflisten von WMI mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="6a91c-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="6a91c-116">Auflisten von WMI mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="6a91c-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="6a91c-117">Auflisten von WMI mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a91c-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="6a91c-118">Wenn Sie den Objekt Pfad für eine bestimmte Instanz nicht kennen oder alle Instanzen für eine bestimmte Klasse abrufen möchten, verwenden Sie [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)mit dem Namen der Klasse im *-Class-* Parameter.</span><span class="sxs-lookup"><span data-stu-id="6a91c-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="6a91c-119">Wenn Sie eine Abfrage verwenden möchten, können Sie den *-Query-* Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="6a91c-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="6a91c-120">Im folgenden Verfahren wird beschrieben, wie die Instanzen einer Klasse mithilfe von PowerShell aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="6a91c-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="6a91c-121">**So zählen Sie die Instanzen einer Klasse mithilfe von PowerShell auf**</span><span class="sxs-lookup"><span data-stu-id="6a91c-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="6a91c-122">Zählen Sie die Instanzen mit einem [Get-WMIObject-](https://technet.microsoft.com/library/dd315379.aspx) Cmdlet auf.</span><span class="sxs-lookup"><span data-stu-id="6a91c-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="6a91c-123">[Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) gibt eine Auflistung von einem oder mehreren WMI-Objekten zurück, die Sie auflisten können.</span><span class="sxs-lookup"><span data-stu-id="6a91c-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="6a91c-124">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="6a91c-125">Wenn Sie eine WMI-Klasseninstanz in einem anderen Namespace oder auf einem anderen Computer abrufen möchten, geben Sie den Computer und den Namespace in den Parametern " *-Computer* " bzw. " *-Namespace* " an.</span><span class="sxs-lookup"><span data-stu-id="6a91c-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="6a91c-126">Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="6a91c-127">Dies funktioniert nur, wenn Sie über die entsprechenden Zugriffsberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="6a91c-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="6a91c-128">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="6a91c-129">Rufen Sie alle einzelnen Instanzen, die Sie wünschen, mithilfe der Member der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="6a91c-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="6a91c-130">Das folgende Codebeispiel ruft eine PowerShell-Sammlung ab und zeigt dann die Size-Eigenschaft für alle Instanzen logischer Laufwerke auf dem lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="6a91c-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="6a91c-131">Auflisten von WMI mit c# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="6a91c-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="6a91c-132">Fügen Sie einen Verweis auf die Verweisassembly **Microsoft. Management. Infrastructure** hinzu.</span><span class="sxs-lookup"><span data-stu-id="6a91c-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="6a91c-133">(Diese Assembly wird als Teil des [Windows Software Development Kit (SDK) für Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)ausgeliefert.)</span><span class="sxs-lookup"><span data-stu-id="6a91c-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="6a91c-134">Fügen Sie eine **using** -Anweisung für den **Microsoft. Management. Infrastructure** -Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="6a91c-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="6a91c-135">Instanziieren Sie ein [cimsession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6a91c-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="6a91c-136">Im folgenden Code Ausschnitt wird der Standardwert "localhost" für die [**cimsession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a91c-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="6a91c-137">Wenden Sie die Methode [**cimsession. queryinstance**](https://www.bing.com/search?q=**CimSession.QueryInstances**) an, und übergeben Sie den gewünschten CIM-Namespace und die zu verwendende WQL.</span><span class="sxs-lookup"><span data-stu-id="6a91c-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="6a91c-138">Der folgende Code Ausschnitt gibt zwei-Instanzen zurück, die zwei standardmäßige Windows-Prozesse darstellen, bei denen die Handle-Eigenschaft (die eine Prozess-ID oder PID darstellt) den Wert 0 oder 4 hat.</span><span class="sxs-lookup"><span data-stu-id="6a91c-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="6a91c-139">Durchlaufen der zurückgegebenen [**ciminstance**](https://www.bing.com/search?q=**CimInstance**) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="6a91c-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="6a91c-140">Im folgenden Codebeispiel werden alle Instanzen der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse (die aktive Prozesse darstellt) auf dem lokalen Computer aufgelistet, und die Namen der einzelnen Prozesse werden gedruckt.</span><span class="sxs-lookup"><span data-stu-id="6a91c-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="6a91c-141">In einer echten Anwendung würden Sie als Parameter den Computernamen ("localhost") und den CIM-Namespace ("root \\ CIMV2") definieren.</span><span class="sxs-lookup"><span data-stu-id="6a91c-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="6a91c-142">Aus Gründen der Einfachheit wurden diese in diesem Beispiel hart codiert.</span><span class="sxs-lookup"><span data-stu-id="6a91c-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="6a91c-143">Auflisten von WMI mit c# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="6a91c-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="6a91c-144">Wenn Sie den Objekt Pfad für eine bestimmte Instanz nicht kennen oder alle Instanzen für eine bestimmte Klasse abrufen möchten, verwenden Sie das [ManagementClass](/dotnet/api/system.management.managementclass) -Objekt, um eine [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) abzurufen, die alle Instanzen einer bestimmten Klasse im WMI-Namespace enthält.</span><span class="sxs-lookup"><span data-stu-id="6a91c-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="6a91c-145">Alternativ können Sie WMI über einen [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) Abfragen, um denselben Satz von Objekten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a91c-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="6a91c-146">**System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.</span><span class="sxs-lookup"><span data-stu-id="6a91c-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="6a91c-147">Im folgenden Verfahren wird beschrieben, wie die Instanzen einer Klasse mit c# aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="6a91c-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="6a91c-148">**So zählen Sie die Instanzen einer Klasse mithilfe von C auf #**</span><span class="sxs-lookup"><span data-stu-id="6a91c-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="6a91c-149">Auflisten der-Instanzen mit einem-Befehl von [ManagementClass. getinhaltungen](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span><span class="sxs-lookup"><span data-stu-id="6a91c-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="6a91c-150">Die [getinhaltungen](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) -Methode gibt eine Auflistung von Objekten zurück, die Sie auflisten können, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="6a91c-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="6a91c-151">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="6a91c-152">Die zurückgegebene Auflistung ist tatsächlich ein [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) -Objekt, sodass jede Methode dieses Objekts aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a91c-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="6a91c-153">Wenn Sie eine WMI-Klasseninstanz in einem anderen Namespace oder auf einem anderen Computer abrufen möchten, geben Sie den Computer und den Namespace im *path* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="6a91c-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="6a91c-154">Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="6a91c-155">Dies funktioniert nur, wenn Sie über die entsprechenden Zugriffsberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="6a91c-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="6a91c-156">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="6a91c-157">Rufen Sie alle einzelnen Instanzen, die Sie wünschen, mithilfe der Member der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="6a91c-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="6a91c-158">Im folgenden Codebeispiel wird eine c#-Auflistung abgerufen und anschließend die Size-Eigenschaft für alle Instanzen von logischen Laufwerken auf dem lokalen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a91c-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="6a91c-159">Auflisten von WMI mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="6a91c-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="6a91c-160">Wenn Sie den Objekt Pfad für eine bestimmte Instanz nicht kennen oder alle Instanzen für eine bestimmte Klasse abrufen möchten, verwenden Sie die Methode " [**errbemservices. InstancesOf**](swbemservices-instancesof.md) ", um eine " [**slibewbjectset**](swbemobjectset.md) "-Enumeration aller Instanzen einer Klasse zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6a91c-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="6a91c-161">Alternativ können Sie WMI über [**SWbemServices.Execquery**](swbemservices-execquery.md) Abfragen, um denselben Satz von Objekten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a91c-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="6a91c-162">Im folgenden Verfahren wird beschrieben, wie die Instanzen einer Klasse mithilfe von VBScript aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="6a91c-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="6a91c-163">**So zählen Sie die Instanzen einer Klasse mithilfe von VBScript auf**</span><span class="sxs-lookup"><span data-stu-id="6a91c-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="6a91c-164">Auflisten der-Instanzen mit einem auflistungsbefehl der Methode " [**Swap Services. InstancesOf**](swbemservices-instancesof.md) ".</span><span class="sxs-lookup"><span data-stu-id="6a91c-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="6a91c-165">Die [**InstancesOf**](swbemservices-instancesof.md) -Methode gibt eine Auflistung von Objekten zurück, die Sie auflisten können, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="6a91c-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="6a91c-166">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="6a91c-167">Die zurückgegebene Auflistung ist tatsächlich ein [**errbewbjectset**](swbemobjectset.md) -Objekt, sodass jede Methode dieses Objekts aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a91c-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="6a91c-168">Wenn Sie eine WMI-Klasseninstanz in einem anderen Namespace oder auf einem anderen Computer abrufen möchten, geben Sie den Computer und den Namespace im Moniker an.</span><span class="sxs-lookup"><span data-stu-id="6a91c-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="6a91c-169">Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="6a91c-170">Dies funktioniert nur, wenn Sie über die entsprechenden Zugriffsberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="6a91c-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="6a91c-171">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="6a91c-172">Rufen Sie mithilfe der Auflistungs Methoden alle einzelnen gewünschten Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="6a91c-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="6a91c-173">Im folgenden Codebeispiel wird ein-Objekt vom Typ " [**Swap Services**](swbemservices.md) " abgerufen und anschließend die [**InstancesOf**](swbemservices-instancesof.md) -Methode ausgeführt, um die Size-Eigenschaft für alle Instanzen von logischen Laufwerken auf dem lokalen Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a91c-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="6a91c-174">Auflisten von WMI mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="6a91c-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="6a91c-175">Zusätzlich zur Durchführung der einfachen Enumeration können Sie mehrere Flags und Eigenschaften festlegen, um die Leistung der Enumeration zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="6a91c-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="6a91c-176">Weitere Informationen finden Sie unter [verbessern der enumerationsleistung](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="6a91c-177">**So zählen Sie einen Objekt Satz in WMI auf**</span><span class="sxs-lookup"><span data-stu-id="6a91c-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="6a91c-178">Erstellen Sie eine [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstelle, die den Satz von Objekten beschreibt, die Sie auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="6a91c-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="6a91c-179">Ein [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Objekt enthält eine Liste, in der ein Satz von WMI-Objekten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6a91c-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="6a91c-180">Sie können die **ienumwbemclassobject** -Methoden verwenden, um vorwärts aufzuzählen, Objekte zu überspringen, am Anfang zu beginnen und den Enumerator zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="6a91c-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="6a91c-181">In der folgenden Tabelle werden die Methoden aufgelistet, die zum Erstellen von Enumeratoren für verschiedene Typen von WMI-Objekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a91c-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6a91c-182">Object</span><span class="sxs-lookup"><span data-stu-id="6a91c-182">Object</span></span></th>
    <th><span data-ttu-id="6a91c-183">Methode</span><span class="sxs-lookup"><span data-stu-id="6a91c-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6a91c-184">Klasse</span><span class="sxs-lookup"><span data-stu-id="6a91c-184">Class</span></span></td>
    <td><dl><span data-ttu-id="6a91c-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: kreateclassenum</strong></a></span><span class="sxs-lookup"><span data-stu-id="6a91c-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="6a91c-186">[<strong>IWbemServices:: feateclassenumschlag</strong>Sequenz] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span><span class="sxs-lookup"><span data-stu-id="6a91c-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6a91c-187">Instanz</span><span class="sxs-lookup"><span data-stu-id="6a91c-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="6a91c-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: kreateinstanceaufumum</strong></a></span><span class="sxs-lookup"><span data-stu-id="6a91c-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="6a91c-189">[<strong>IWbemServices:: "kreateingestanceenumasync</strong>"] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span><span class="sxs-lookup"><span data-stu-id="6a91c-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6a91c-190">Abfrageergebnis</span><span class="sxs-lookup"><span data-stu-id="6a91c-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="6a91c-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="6a91c-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="6a91c-192">[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span><span class="sxs-lookup"><span data-stu-id="6a91c-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6a91c-193">Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6a91c-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="6a91c-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="6a91c-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="6a91c-195">[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span><span class="sxs-lookup"><span data-stu-id="6a91c-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="6a91c-196">Durchlaufen der zurückgegebenen Enumeration mithilfe mehrerer Aufrufe von [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) oder [**ienumwbemclassobject:: nextasync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span><span class="sxs-lookup"><span data-stu-id="6a91c-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="6a91c-197">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="6a91c-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
