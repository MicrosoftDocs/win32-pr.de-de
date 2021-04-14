---
description: Die gängigste Methode, eine WMI-Klasseninstanz zu aktualisieren, besteht darin, die gesamte Instanz gleichzeitig zu aktualisieren.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Aktualisieren einer gesamten Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217115"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="249df-103">Aktualisieren einer gesamten Instanz</span><span class="sxs-lookup"><span data-stu-id="249df-103">Updating an Entire Instance</span></span>

<span data-ttu-id="249df-104">Die gängigste Methode, eine WMI-Klasseninstanz zu aktualisieren, besteht darin, die gesamte Instanz gleichzeitig zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="249df-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="249df-105">Wenn Sie eine gesamte Instanz aktualisieren, muss die Instanz von WMI nicht in einzelne Eigenschaften analysiert und an Ihre Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="249df-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="249df-106">Stattdessen kann WMI Ihnen einfach die gesamte-Instanz senden.</span><span class="sxs-lookup"><span data-stu-id="249df-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="249df-107">Wenn Sie fertig sind, kann die gesamte geänderte Instanz von WMI über die ursprüngliche Instanz kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="249df-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="249df-108">Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mithilfe von PowerShell ändern oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="249df-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="249df-109">**So ändern oder aktualisieren Sie eine Instanz mithilfe von PowerShell**</span><span class="sxs-lookup"><span data-stu-id="249df-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="249df-110">Rufen Sie eine lokale Kopie des Objekts mit einem Get-WMIObject-Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="249df-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="249df-111">Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie die Properties-Auflistung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="249df-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="249df-112">Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.</span><span class="sxs-lookup"><span data-stu-id="249df-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="249df-113">Nehmen Sie Änderungen an den Eigenschaften des lokalen Objekts vor.</span><span class="sxs-lookup"><span data-stu-id="249df-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="249df-114">Dadurch wird nur die lokale Kopie geändert.</span><span class="sxs-lookup"><span data-stu-id="249df-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="249df-115">Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.</span><span class="sxs-lookup"><span data-stu-id="249df-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="249df-116">Versetzen Sie das Objekt mithilfe eines Aufrufens der Put-Methode wieder in das WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="249df-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="249df-117">Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mit c# ändern oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="249df-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="249df-118">**So ändern oder aktualisieren Sie eine Instanz mit c# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="249df-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="249df-119">Rufen Sie eine lokale Kopie des-Objekts mit einem [cimsession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))-Befehl ab, wie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="249df-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="249df-120">Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie die Properties-Auflistung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="249df-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="249df-121">Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.</span><span class="sxs-lookup"><span data-stu-id="249df-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="249df-122">Nehmen Sie Änderungen an den Eigenschaften des lokalen Objekts vor.</span><span class="sxs-lookup"><span data-stu-id="249df-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="249df-123">Dadurch wird nur die lokale Kopie geändert.</span><span class="sxs-lookup"><span data-stu-id="249df-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="249df-124">Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.</span><span class="sxs-lookup"><span data-stu-id="249df-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="249df-125">Versetzen Sie das Objekt mithilfe eines Aufrufens von [cimsession. modifyinstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85))wieder in das WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="249df-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="249df-126">Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mithilfe von PowerShell ändern oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="249df-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="249df-127">**System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.</span><span class="sxs-lookup"><span data-stu-id="249df-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="249df-128">**So ändern oder aktualisieren Sie eine Instanz mit c# (Microsoft. Management)**</span><span class="sxs-lookup"><span data-stu-id="249df-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="249df-129">Rufen Sie eine lokale Kopie des Objekts mit einem-Befehl von [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)ab.</span><span class="sxs-lookup"><span data-stu-id="249df-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="249df-130">Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie die Properties-Auflistung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="249df-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="249df-131">Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.</span><span class="sxs-lookup"><span data-stu-id="249df-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="249df-132">Nehmen Sie Änderungen an den Eigenschaften des lokalen Objekts vor.</span><span class="sxs-lookup"><span data-stu-id="249df-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="249df-133">Dadurch wird nur die lokale Kopie geändert.</span><span class="sxs-lookup"><span data-stu-id="249df-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="249df-134">Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.</span><span class="sxs-lookup"><span data-stu-id="249df-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="249df-135">Versetzen Sie das Objekt mithilfe eines Aufrufens der [ManagementObject. Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) -oder-Methode wieder in das WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="249df-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="249df-136">Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mit VBScript ändern oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="249df-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="249df-137">**So ändern oder aktualisieren Sie eine Instanz mit VBScript**</span><span class="sxs-lookup"><span data-stu-id="249df-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="249df-138">Rufen Sie eine lokale Kopie des Objekts mit einem Aufrufen von **GetObject** ab.</span><span class="sxs-lookup"><span data-stu-id="249df-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="249df-139">Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie [**die \_ Properties**](swbemobject-properties-.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="249df-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="249df-140">Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.</span><span class="sxs-lookup"><span data-stu-id="249df-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="249df-141">Nehmen Sie Änderungen an den Objekteigenschaften vor, indem Sie die Methode " [**Swap-Eigenschaft. Value**](swbemproperty-value.md) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="249df-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="249df-142">Die **value** -Methode ändert nur die lokale Kopie.</span><span class="sxs-lookup"><span data-stu-id="249df-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="249df-143">Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.</span><span class="sxs-lookup"><span data-stu-id="249df-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="249df-144">Versetzen Sie das Objekt wieder in das WMI-Repository, indem Sie die Methoden " [**errbewbject. Put \_**](swbemobject-put-.md) " oder " [**errbewbject. putasync \_**](swbemobject-putasync-.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="249df-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="249df-145">Wie die Namen impliziert, werden Updates synchron [**eingefügt \_**](swbemobject-put-.md) , während [**putasync \_**](swbemobject-putasync-.md) asynchron aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="249df-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="249df-146">Beide Methoden kopieren die ursprüngliche Instanz mit der geänderten Instanz.</span><span class="sxs-lookup"><span data-stu-id="249df-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="249df-147">Um die Nutzung der asynchronen Verarbeitung zu nutzen, müssen Sie jedoch ein " [**taubemsink**](swbemsink.md) "-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="249df-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="249df-148">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="249df-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="249df-149">Im folgenden Verfahren wird beschrieben, wie eine Instanz mit C++ geändert oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="249df-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="249df-150">**So ändern oder aktualisieren Sie eine Instanz mithilfe von C++**</span><span class="sxs-lookup"><span data-stu-id="249df-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="249df-151">Rufen Sie eine lokale Kopie der-Instanz mit einem Befehl zum Aufrufen von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab.</span><span class="sxs-lookup"><span data-stu-id="249df-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="249df-152">Zeigen Sie ggf. die Eigenschaften des Objekts mit einem Befehl an, um [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="249df-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="249df-153">Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.</span><span class="sxs-lookup"><span data-stu-id="249df-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="249df-154">Nehmen Sie alle notwendigen Änderungen an der Kopie mit einem Befehl [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)vor.</span><span class="sxs-lookup"><span data-stu-id="249df-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="249df-155">Mit der **Put** -Methode wird nur die lokale Kopie geändert.</span><span class="sxs-lookup"><span data-stu-id="249df-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="249df-156">Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.</span><span class="sxs-lookup"><span data-stu-id="249df-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="249df-157">Fügen Sie die Kopie zurück in das WMI-Repository ein, indem Sie die Methoden [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="249df-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="249df-158">Wie die Namen impliziert, aktualisiert **PutInstance** synchron, während [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) asynchron aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="249df-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="249df-159">Beide Methoden kopieren die ursprüngliche Instanz mit der geänderten Instanz.</span><span class="sxs-lookup"><span data-stu-id="249df-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="249df-160">Um die asynchrone Verarbeitung zu nutzen, müssen Sie jedoch die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="249df-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="249df-161">Beachten Sie, dass ein Aktualisierungs Vorgang für eine Instanz, die zu einer Klassenhierarchie gehört, aufgrund eines Fehlers, der eine andere Klasse in der Hierarchie einschließt, möglicherweise nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="249df-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="249df-162">WMI Ruft die [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) -Methode für jeden Anbieter auf, der für die Klassen verantwortlich ist, von denen die Klasse, die die ursprüngliche Instanz besitzt, abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="249df-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="249df-163">Wenn einer dieser Anbieter ausfällt, tritt bei der ursprünglichen Update Anforderung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="249df-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="249df-164">Weitere Informationen finden Sie im Abschnitt "Hinweise" von [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="249df-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="249df-165">Weitere Informationen finden Sie unter [Aufrufen einer Anbieter Methode](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="249df-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="249df-166">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="249df-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="249df-167">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="249df-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 
