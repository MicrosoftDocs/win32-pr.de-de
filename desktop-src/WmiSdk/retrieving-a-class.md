---
description: Der erste Objekttyp, den Sie abrufen können, ist eine WMI-Klasse.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Abrufen einer WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106354918"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="9b277-103">Abrufen einer WMI-Klasse</span><span class="sxs-lookup"><span data-stu-id="9b277-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="9b277-104">Der erste Objekttyp, den Sie abrufen können, ist eine WMI-Klasse.</span><span class="sxs-lookup"><span data-stu-id="9b277-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="9b277-105">Wenn Sie eine WMI-Klasse abrufen, rufen Sie tatsächlich eine Klassendefinition ab, die eine Auflistung der Eigenschaften, Qualifizierer und Methoden ist, die die Klasse vollständig beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b277-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="9b277-106">Eine Klassendefinition ist jedoch im Grunde die Klasse selbst.</span><span class="sxs-lookup"><span data-stu-id="9b277-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="9b277-107">PowerShell verwendet eine Standard Abfrage zum Abrufen von Klassendefinitionen mithilfe der **Meta \_ Class** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="9b277-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="9b277-108">**So rufen Sie eine Klassendefinition in PowerShell ab**</span><span class="sxs-lookup"><span data-stu-id="9b277-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="9b277-109">Verwenden Sie das [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) mit einer Abfrage an eine **Meta- \_ Klasse** mit der WHERE-Klausel, die den Namen der Klasse enthält, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b277-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="9b277-110">[Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) ist das Standard-Cmdlet, das PowerShell verwendet, um Klassen-und Instanzinformationen aus WMI abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b277-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="9b277-111">Die **Meta \_ Class** -Klasse definiert die Abfrage als Schema Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9b277-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="9b277-112">Ohne die **Meta \_ Class** -Klasse würde diese Abfrage alle Instanzen von Win32 \_ LogicalDisk zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9b277-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="9b277-113">Weitere Informationen zum Abfragen von WMI finden Sie unter [SELECT-Anweisung für Schema Abfragen](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="9b277-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="9b277-114">Der aktuelle Prozess zum Abrufen einer WMI-Definition in c# ist die Verwendung der **ciminstance** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="9b277-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="9b277-115">**So rufen Sie eine Klassendefinition in c# ab (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="9b277-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="9b277-116">Erstellen Sie mithilfe des **Microsoft. Management. Infrastructure** -Namespace eine **ciminstance** -Klasse mit dem angegebenen Namespace und dem Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="9b277-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="9b277-117">Die erstellte Klasse enthält alle Klassen Informationen, aber keine Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="9b277-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="9b277-118">Alternativ können Sie wie bei PowerShell auch eine Abfrage durchführen, indem Sie das **Meta- \_ klassentag** als Teil der Abfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b277-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="9b277-119">Wie bei PowerShell verwendet c# eine **Meta- \_ Klassen** Abfrage zum Abrufen von Klassendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9b277-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="9b277-120">Alternativ können Sie ein **ManagementClass** -Objekt erstellen, um direkt auf die Klassendefinition zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9b277-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="9b277-121">**System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.</span><span class="sxs-lookup"><span data-stu-id="9b277-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="9b277-122">**So rufen Sie eine Klassendefinition in c# ab (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="9b277-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="9b277-123">Sie können [managementobjectserarcher](/dotnet/api/system.management.managementobjectsearcher) mit einer Abfrage an eine **Meta- \_ Klasse** mit der WHERE-Klausel verwenden, die den Namen der Klasse enthält, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b277-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="9b277-124">[Managementobjectserarcher](/dotnet/api/system.management.managementobjectsearcher) ist die Standardklasse, die .NET verwendet, um Klassen-und Instanzinformationen aus WMI abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b277-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="9b277-125">[Managementobjectserarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) gibt eine [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) zurück, die die Schema Definitions Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="9b277-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="9b277-126">Die **Meta \_ Class** -Klasse definiert die Abfrage als Schema Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9b277-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="9b277-127">Ohne die **Meta \_ Class** -Klasse würde diese Abfrage alle Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9b277-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="9b277-128">Weitere Informationen zum Abfragen von WMI finden Sie unter [SELECT-Anweisung für Schema Abfragen](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="9b277-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="9b277-129">Erstellen Sie alternativ ein neues [ManagementClass](/dotnet/api/system.management.managementclass) -Objekt mit dem Namen als Pfad, um die Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b277-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="9b277-130">Sie können eine Klassendefinition in VBScript auf ähnliche Weise abrufen, um eine bestimmte Instanz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b277-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="9b277-131">**So rufen Sie eine Klassendefinition in VBScript ab**</span><span class="sxs-lookup"><span data-stu-id="9b277-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="9b277-132">Ruft die Methode " [**Austausch Services. Get**](swbemservices-get.md) " auf, identifiziert aber keine bestimmte Instanz im Objekt Pfad für die Klasse.</span><span class="sxs-lookup"><span data-stu-id="9b277-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="9b277-133">Das folgende Codebeispiel ruft die Klassendefinition für die-Klasse ab, die logische Laufwerke auf Ihrem Computer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9b277-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="9b277-134">Windows Script Host (WSH) unterstützt auch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9b277-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="9b277-135">Verwenden Sie auf Active Server Seiten (ASP) [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) oder [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) im Server seitigen Skript.</span><span class="sxs-lookup"><span data-stu-id="9b277-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="9b277-136">Weitere Informationen finden Sie unter [Erstellen von Active Server Seiten für WMI](creating-active-server-pages-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9b277-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="9b277-137">Es kann auch eine Klasse oder eine Instanz angegeben werden. in diesem Fall handelt es sich bei dem zurückgegebenen Objekt um ein WMI-Objekt, z. b. eine Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), anstatt um ein Dienst Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b277-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="9b277-138">Beachten Sie, dass Sie die [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) -Funktionen von VBScript nicht verwenden können, um eine Instanz des generischen Objekts " [**errbewbject**](swbemobject.md)" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b277-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="9b277-139">In HTML-Seiten, die in Microsoft Internet Explorer (IE) ausgeführt werden, können [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) und [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) fehlschlagen, da WMI-Skript Objekte, wie z. b. ActiveX-Steuerelemente, nicht als sichere Skripts gekennzeichnet sind</span><span class="sxs-lookup"><span data-stu-id="9b277-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="9b277-140">Die einzige Ausnahme ist das Objekt " [**taubemdatetime**](swbemdatetime.md) ".</span><span class="sxs-lookup"><span data-stu-id="9b277-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="9b277-141">Diese Aufrufe können nur dann erfolgreich ausgeführt werden, wenn Sie die Internet Explorer-Sicherheitseinstellungen verringern, was nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="9b277-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="9b277-142">Wenn Sie eine Klasse in C++ abrufen, rufen Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Version von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)auf.</span><span class="sxs-lookup"><span data-stu-id="9b277-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="9b277-143">**So rufen Sie eine Klassendefinition in C++ ab**</span><span class="sxs-lookup"><span data-stu-id="9b277-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="9b277-144">Rufen Sie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode oder die [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode auf, um die Definition einer Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b277-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="9b277-145">Eine Klasse kann über mehrere Klassendefinitionen verfügen. Dies geschieht in der Regel, wenn Sie mehr als einen Klassen Anbieter in einen Namespace geladen haben.</span><span class="sxs-lookup"><span data-stu-id="9b277-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="9b277-146">Wenn eine Klasse über mehrere Klassendefinitionen verfügt, gibt WMI die erkannte erste Definition und den Statuscode der **WBEM \_ S- \_ \_ Objekte dupliziert** zurück.</span><span class="sxs-lookup"><span data-stu-id="9b277-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="9b277-147">Da [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) eine Klassendefinition zurückgibt, wird diese häufig als erster Schritt beim Erstellen einer Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b277-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="9b277-148">Weitere Informationen zur Verwendung von **GetObject** finden [Sie unter Erstellen und Deklarieren einer Instanz mithilfe von C++](creating-and-declaring-an-instance-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="9b277-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 
