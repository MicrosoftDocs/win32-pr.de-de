---
description: Bei einer synchronen Abfrage handelt es sich um eine Abfrage, die die Kontrolle über den Prozess der Anwendung für die Dauer der Abfrage behält.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Aufrufen einer synchronen Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362980"
---
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="9e537-103">Aufrufen einer synchronen Abfrage</span><span class="sxs-lookup"><span data-stu-id="9e537-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="9e537-104">Bei einer synchronen Abfrage handelt es sich um eine Abfrage, die die Kontrolle über den Prozess der Anwendung für die Dauer der Abfrage behält.</span><span class="sxs-lookup"><span data-stu-id="9e537-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="9e537-105">Eine synchrone Abfrage erfordert einen einzelnen Schnittstellen Rückruf und ist daher einfacher als ein asynchroner-Befehl.</span><span class="sxs-lookup"><span data-stu-id="9e537-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="9e537-106">Eine synchrone Abfrage hat jedoch die Möglichkeit, Ihre Anwendung für große Abfragen oder Abfragen über ein Netzwerk zu sperren.</span><span class="sxs-lookup"><span data-stu-id="9e537-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="9e537-107">Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mithilfe von PowerShell ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e537-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="9e537-108">**So geben Sie eine synchrone Datenabfrage in PowerShell aus**</span><span class="sxs-lookup"><span data-stu-id="9e537-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="9e537-109">Beschreiben Sie die WMI-Abfrage mithilfe des WMI-Cmdlets [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) und des *-Query-* Parameters.</span><span class="sxs-lookup"><span data-stu-id="9e537-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="9e537-110">Das-Cmdlet gibt entweder ein einzelnes-Objekt oder eine Auflistung von-Objekten zurück, abhängig von der Anzahl der Objekte, die der Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9e537-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="9e537-111">Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mit c# ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e537-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="9e537-112">**So geben Sie eine synchrone Datenabfrage in c# aus (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="9e537-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="9e537-113">Beschreiben Sie Ihre Abfrage mit "cimsession. queryinstance" in WMI.</span><span class="sxs-lookup"><span data-stu-id="9e537-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="9e537-114">Diese Methode gibt eine Auflistung von ciminstance-Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="9e537-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="9e537-115">Verwenden Sie standardmäßige c#-sprach Erfassungs Techniken für den Zugriff auf jedes zurückgegebene Objekt</span><span class="sxs-lookup"><span data-stu-id="9e537-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="9e537-116">Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mit c# ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e537-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="9e537-117">**So geben Sie eine synchrone Datenabfrage in c# aus (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="9e537-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="9e537-118">Erstellen Sie die Abfrage mit einem [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) -Objekt, und rufen Sie die Informationen mit einem Aufrufen von [ManagementObjectSearcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get)ab.</span><span class="sxs-lookup"><span data-stu-id="9e537-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="9e537-119">Diese Methode gibt ein [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9e537-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="9e537-120">Verwenden Sie standardmäßige c#-sprach Erfassungs Techniken für den Zugriff auf jedes zurückgegebene Objekt</span><span class="sxs-lookup"><span data-stu-id="9e537-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="9e537-121">Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mithilfe von VBScript ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e537-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="9e537-122">**So geben Sie eine synchrone Datenabfrage in VBScript aus**</span><span class="sxs-lookup"><span data-stu-id="9e537-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="9e537-123">Beschreiben Sie die WMI-Abfrage mit [**SWbemServices.Execquery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="9e537-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="9e537-124">Diese Methode gibt ein " [**errbemubjectset**](swbemobjectset.md)" zurück.</span><span class="sxs-lookup"><span data-stu-id="9e537-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="9e537-125">Verwenden Sie Standard Skripts zur [Skript sprach Auflistung](accessing-a-collection.md) , um auf jedes zurückgegebene Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9e537-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="9e537-126">Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mithilfe von C++ ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e537-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="9e537-127">**So geben Sie eine synchrone Abfrage in C++ aus**</span><span class="sxs-lookup"><span data-stu-id="9e537-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="9e537-128">Beschreiben Sie Ihre Abfrage für WMI durch einen Befehl von [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="9e537-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="9e537-129">Die [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) -Methode nimmt eine WQL-Such Zeichenfolge als Parameter an, der die Abfrage beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e537-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="9e537-130">WMI führt die Abfrage aus und gibt einen [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="9e537-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="9e537-131">Über die **ienumwbemclassobject** -Schnittstelle können Sie auf die Klassen oder Instanzen zugreifen, aus denen das Resultset besteht.</span><span class="sxs-lookup"><span data-stu-id="9e537-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="9e537-132">Nachdem Sie die Abfrage erhalten haben, können Sie die Abfrage mit einem [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)-Rückruf auflisten.</span><span class="sxs-lookup"><span data-stu-id="9e537-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="9e537-133">Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9e537-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="9e537-134">Für das folgende Codebeispiel sind die folgenden Verweise und \# include-Anweisungen erforderlich, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="9e537-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="9e537-135">Im folgenden Codebeispiel wird beschrieben, wie die-Objekte, die die Benutzer und Gruppen in WMI darstellen, abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="9e537-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
