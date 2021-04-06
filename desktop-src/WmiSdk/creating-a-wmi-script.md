---
description: Mithilfe von Skripts können Sie alle Informationen anzeigen oder bearbeiten, die über WMI verfügbar gemacht werden.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Erstellen eines WMI-Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960894"
---
# <a name="creating-a-wmi-script"></a><span data-ttu-id="c9977-103">Erstellen eines WMI-Skripts</span><span class="sxs-lookup"><span data-stu-id="c9977-103">Creating a WMI Script</span></span>

<span data-ttu-id="c9977-104">Mithilfe von Skripts können Sie alle Informationen anzeigen oder bearbeiten, die über WMI verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="c9977-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="c9977-105">Skripts können in jeder Skriptsprache geschrieben werden, die das Hosting von Microsoft-ActiveX-Skripts unterstützt, einschließlich Visual Basic Scripting Edition (VBScript), PowerShell und perl.</span><span class="sxs-lookup"><span data-stu-id="c9977-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="c9977-106">WMI-Skripts können von Windows Script Host (WSH), Active Server Seiten und Internet Explorer gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="c9977-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="c9977-107">Die primäre Skriptsprache, die derzeit von WMI unterstützt wird, ist PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9977-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="c9977-108">WMI enthält jedoch auch einen robusten Text der Skriptunterstützung für VBScript und andere Sprachen, die auf die [Skript-API für WMI](scripting-api-for-wmi.md)zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c9977-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="c9977-109">WMI-Skriptsprachen</span><span class="sxs-lookup"><span data-stu-id="c9977-109">WMI Scripting Languages</span></span>

<span data-ttu-id="c9977-110">Die zwei Hauptsprachen, die von WMI unterstützt werden, sind PowerShell und VBScript (über den Windows Script Host oder WSH).</span><span class="sxs-lookup"><span data-stu-id="c9977-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="c9977-111">**PowerShell** wurde mit einer engen Integration in WMI entworfen.</span><span class="sxs-lookup"><span data-stu-id="c9977-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="c9977-112">Daher sind viele der zugrunde liegenden Elemente von WMI in die WMI-Cmdlets integriert: [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Aufruf-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)und [Remove-WMIObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span><span class="sxs-lookup"><span data-stu-id="c9977-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="c9977-113">In der folgenden Tabelle werden die allgemeinen Prozesse für den Zugriff auf WMI-Informationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c9977-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="c9977-114">Beachten Sie, dass zwar die meisten dieser Beispiele Get-WMIObject verwenden, aber viele der PowerShell-WMI-Cmdlets dieselben Parameter haben, wie z. b. *-Class* oder *--Anmelde* Informationen.</span><span class="sxs-lookup"><span data-stu-id="c9977-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="c9977-115">Daher funktionieren viele dieser Prozesse auch für andere Objekte.</span><span class="sxs-lookup"><span data-stu-id="c9977-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="c9977-116">Eine ausführlichere Erläuterung von PowerShell und WMI finden [Sie unter Verwenden des Get-WMiObject Cmdlets](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) und [Windows PowerShell-der WMI-Verbindung](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c9977-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="c9977-117">**VBScript** führt dagegen explizit Aufrufe an die [Skript-API für WMI aus](scripting-api-for-wmi.md), wie oben erwähnt.</span><span class="sxs-lookup"><span data-stu-id="c9977-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="c9977-118">Andere Sprachen, wie z. b. perl, können auch die Skript-API für WMI verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9977-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="c9977-119">Im Rahmen dieser Dokumentation wird jedoch in den meisten Beispielen, die die Skript-API für WMI veranschaulichen, VBScript verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9977-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="c9977-120">Wenn ein Programmierverfahren für VBScript spezifisch ist, wird es jedoch als "out" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c9977-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="c9977-121">VBScript bietet im Wesentlichen zwei separate Möglichkeiten für den Zugriff auf WMI.</span><span class="sxs-lookup"><span data-stu-id="c9977-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="c9977-122">Der erste verwendet zum Herstellen einer Verbindung mit WMI ein "WS- [**Locator**](swbemlocator.md) "-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c9977-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="c9977-123">Alternativ können Sie [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) und einen Moniker verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9977-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="c9977-124">Ein Moniker ist eine Zeichenfolge, die eine Reihe von Elementen beschreiben kann: Ihre Anmelde Informationen, die Identitätswechsel Einstellungen, den Computer, mit dem Sie eine Verbindung herstellen möchten, den WMI- [*Namespace*](gloss-n.md) (d.h. den allgemeinen Speicherort, an dem WMI Gruppen von Objekten speichert) und das WMI-Objekt, das Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c9977-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="c9977-125">Viele der Beispiele unten beschreiben beide Techniken.</span><span class="sxs-lookup"><span data-stu-id="c9977-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="c9977-126">Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md) und [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="c9977-127">Unabhängig von der Methode, die Sie zum Herstellen einer Verbindung mit WMI verwenden, werden Sie wahrscheinlich ein oder mehrere Objekte aus der Skript-API abrufen.</span><span class="sxs-lookup"><span data-stu-id="c9977-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="c9977-128">Der häufigste Wert ist " [**errbewbject**](swbemobject.md)", der von WMI zum Beschreiben eines WMI-Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9977-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="c9977-129">Alternativ dazu können Sie ein " [**errbemservices**](swbemservices.md) "-Objekt verwenden, um den WMI-Dienst selbst zu beschreiben, oder ein " [**errbewbjectpath**](swbemobjectpath.md) "-Objekt, um den Speicherort eines WMI-Objekts zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c9977-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="c9977-130">Weitere Informationen finden Sie unter [Skripterstellung mit "Swap](scripting-with-swbemobject.md) Helper"- [Objekten](scripting-helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="c9977-131">Gewusst wie: Verwenden von WMI und einer Skriptsprache</span><span class="sxs-lookup"><span data-stu-id="c9977-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="c9977-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... Verbindung mit WMI herstellen?</span><span class="sxs-lookup"><span data-stu-id="c9977-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-133">Rufen Sie für VBScript und die Skript-API für WMI ein [**-Objekt mit einem**](swbemservices.md) Moniker und einem Aufruf von [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))ab.</span><span class="sxs-lookup"><span data-stu-id="c9977-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="c9977-134">Alternativ können Sie eine Verbindung mit dem Server herstellen, indem Sie den [**Befehl "Swap-Server. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9977-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="c9977-135">Anschließend können Sie das-Objekt verwenden, um auf einen bestimmten WMI-Namespace oder eine bestimmte WMI-Klasseninstanz zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c9977-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="c9977-136">Für PowerShell erfolgt die Verbindung mit WMI in der Regel direkt im Cmdlet-Befehl. Daher sind keine weiteren Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c9977-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="c9977-137">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md), [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md)und [Herstellen einer Verbindung mit WMI mit VBScript](connecting-to-wmi-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span data-ttu-id="c9977-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... Abrufen von Informationen aus WMI</span><span class="sxs-lookup"><span data-stu-id="c9977-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-139">Verwenden Sie für VBScript und die Skript-API für WMI eine Abruf Funktion, z. b. [**wbemServices. Get**](swbemservices-get.md) oder [**wbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="c9977-140">Sie können auch den Klassennamen des Objekts platzieren, das in einem Moniker abgerufen werden kann. Dies kann effizienter sein.</span><span class="sxs-lookup"><span data-stu-id="c9977-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="c9977-141">Verwenden Sie für PowerShell den *-Class-* Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9977-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="c9977-142">Beachten Sie, dass-Class der Standardparameter ist. Daher müssen Sie ihn nicht explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="c9977-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="c9977-143">Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span data-ttu-id="c9977-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... Erstellen Sie eine WMI-Abfrage?</span><span class="sxs-lookup"><span data-stu-id="c9977-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-145">Verwenden Sie für VBScript und die Skript-API für WMI die [**SWbemServices.Execquery**](swbemservices-execquery.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c9977-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="c9977-146">Verwenden Sie für PowerShell den *-Query-* Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9977-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="c9977-147">Sie können auch mit dem *-Filter-* Parameter filtern.</span><span class="sxs-lookup"><span data-stu-id="c9977-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="c9977-148">Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span data-ttu-id="c9977-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... durchlaufen Sie eine Liste von WMI-Objekten?</span><span class="sxs-lookup"><span data-stu-id="c9977-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-150">Verwenden Sie für VBScript und die Skript-API für WMI das in einem Skript behandelte Objekt " [**errbewbjectset**](swbemobjectset.md) " als eine Auflistung, die aufgelistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9977-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="c9977-151">Sie können ein " **errbemubjectset** " aus einem- [**Befehl von "errbemservices. InstancesOf**](swbemservices-instancesof.md) " oder [**SWbemServices.Execquery**](swbemservices-execquery.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="c9977-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="c9977-152">PowerShell kann Enumerationen wie jedes andere Objekt abrufen und verarbeiten. Es gibt keine besonderen Besonderheiten bei WMI.</span><span class="sxs-lookup"><span data-stu-id="c9977-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="c9977-153">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span data-ttu-id="c9977-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... greifen Sie auf einen anderen WMI-Namespace zu?</span><span class="sxs-lookup"><span data-stu-id="c9977-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-155">Geben Sie für VBScript und die Skript-API für WMI den Namespace im Moniker an. andernfalls können Sie den Namespace im Aufruf von "WS. [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="c9977-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="c9977-156">Verwenden Sie für PowerShell den Parameter *-Namespace* .</span><span class="sxs-lookup"><span data-stu-id="c9977-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="c9977-157">Der Standard Namespace ist "root \\ cimV2", aber viele ältere Klassen werden in "root \\ default" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c9977-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="c9977-158">Wenn Sie den Speicherort einer bestimmten WMI-Klasse ermitteln möchten, sehen Sie sich die Referenzseite an.</span><span class="sxs-lookup"><span data-stu-id="c9977-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="c9977-159">Alternativ können Sie einen Namespace mithilfe von Get-WMIObject manuell durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="c9977-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span data-ttu-id="c9977-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... alle untergeordneten Instanzen einer Klasse abrufen?</span><span class="sxs-lookup"><span data-stu-id="c9977-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-161">Für Sprachen, die die Skript-API für WMI und PowerShell direkt verwenden, unterstützt WMI das Abrufen der untergeordneten Klassen einer Basisklasse.</span><span class="sxs-lookup"><span data-stu-id="c9977-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="c9977-162">Um die untergeordneten Instanzen abzurufen, müssen Sie daher nur nach der übergeordneten Klasse suchen.</span><span class="sxs-lookup"><span data-stu-id="c9977-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="c9977-163">Im folgenden Beispiel wird nach [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)gesucht. Hierbei handelt es sich um eine vorinstallierte WMI-Klasse, die logische Datenträger auf einem Windows-basierten Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="c9977-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="c9977-164">Daher gibt die Suche nach dieser übergeordneten Klasse auch Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)zurück. Dies ist das, was von Windows verwendet wird, um Festplatten zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c9977-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="c9977-165">Weitere Informationen finden Sie unter [Common Information Model](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="c9977-166">WMI stellt ein gesamtes Schema mit vorinstallierten Klassen bereit, mit denen Sie auf verwaltete Objekte zugreifen und diese steuern können.</span><span class="sxs-lookup"><span data-stu-id="c9977-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="c9977-167">Weitere Informationen finden Sie unter [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider) und [WMI-Klassen](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="c9977-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... Suchen Sie ein WMI-Objekt?</span><span class="sxs-lookup"><span data-stu-id="c9977-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-169">Bei der Skript-API für WMI und PowerShell verwendet WMI eine Kombination aus Namespace, Klassenname und Schlüsseleigenschaften, um eine bestimmte WMI-Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c9977-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="c9977-170">Dies wird auch als WMI-Objekt Pfad bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c9977-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="c9977-171">Für VBScript beschreibt die Eigenschaft " [**Swap. Path \_**](swbemobject-path-.md) " den Pfad für ein beliebiges Objekt, das von der Skript-API zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9977-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="c9977-172">Für PowerShell verfügt jedes WMI-Objekt über eine \_ \_ Path-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c9977-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="c9977-173">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c9977-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="c9977-174">Neben dem Namespace-und Klassennamen verfügt ein WMI-Objekt auch über eine Schlüsseleigenschaft, die diese Instanz im Vergleich zu anderen Instanzen auf dem Computer eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c9977-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="c9977-175">Die **DeviceID** -Eigenschaft ist z. b. die Schlüsseleigenschaft für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="c9977-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="c9977-176">Weitere Informationen finden Sie unter [Managed Object Format (MOF)](managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="c9977-177">Schließlich ist der relative Pfad einfach eine verkürzte Form des Pfads und enthält den Klassennamen und den Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="c9977-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="c9977-178">In den folgenden Beispielen lautet der Pfad möglicherweise " \\ \\ Computername \\ root \\ CIMV2: Win32 \_ LogicalDisk. toviceid =" D: "", während der relative Pfad "" Win32LogicalDisk. Geräte-ID = "d" "" lauten würde.</span><span class="sxs-lookup"><span data-stu-id="c9977-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span data-ttu-id="c9977-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... Legen Sie Informationen in WMI fest?</span><span class="sxs-lookup"><span data-stu-id="c9977-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-180">Verwenden Sie für VBScript und die Skript-API für WMI die Methode " [**errbemubject. Put \_**](swbemobject-put-.md) ".</span><span class="sxs-lookup"><span data-stu-id="c9977-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="c9977-181">Für PowerShell können Sie entweder die Put-Methode oder Else [Set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9977-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="c9977-182">Weitere Informationen finden Sie unter [Ändern einer Instanzeigenschaft](modifying-an-instance-property.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span data-ttu-id="c9977-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... Andere Anmelde Informationen verwenden?</span><span class="sxs-lookup"><span data-stu-id="c9977-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-184">Verwenden Sie für VBScript und die Skript-API für WMI die Parameter " *username* " und " *Password* " in der Methode " [**waybemlocator. ConnectServer**](swbemlocator-connectserver.md) ".</span><span class="sxs-lookup"><span data-stu-id="c9977-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="c9977-185">Verwenden Sie für PowerShell den *-Credential-* Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9977-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="c9977-186">Beachten Sie, dass Sie nur Alternative Anmelde Informationen auf einem Remote System verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c9977-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="c9977-187">Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="c9977-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... auf einen Remote Computer zugreifen?</span><span class="sxs-lookup"><span data-stu-id="c9977-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-189">Geben Sie für VBScript und die Skript-API für WMI explizit den Namen des Computers entweder im Moniker oder andernfalls im Aufruf von "WS. [**ConnectServer**](swbemlocator-connectserver.md)" an.</span><span class="sxs-lookup"><span data-stu-id="c9977-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="c9977-190">Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI mit VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="c9977-191">Verwenden Sie für PowerShell den Parameter " *-Computername* ".</span><span class="sxs-lookup"><span data-stu-id="c9977-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="c9977-192">Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI mit PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="c9977-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... Legen Sie die Authentifizierungs-und Identitätswechsel Ebenen fest?</span><span class="sxs-lookup"><span data-stu-id="c9977-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-194">Verwenden Sie für VBScript und die Skript-API für WMI die Eigenschaft " [**Swap Services \_ . Security**](swbemlocator-security-.md) " für das zurückgegebene Server Objekt, oder legen Sie die relevanten Werte im Moniker fest.</span><span class="sxs-lookup"><span data-stu-id="c9977-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="c9977-195">Verwenden Sie für PowerShell die Parameter *-Authentication* bzw. *-* Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="c9977-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="c9977-196">Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="c9977-197">Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="c9977-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... Behandeln von Fehlern in WMI</span><span class="sxs-lookup"><span data-stu-id="c9977-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="c9977-199">Der Anbieter kann für die Skript-API für WMI ein " [**taubemlasterror**](swbemlasterror.md) "-Objekt bereitstellen, um weitere Informationen zu einem Fehler zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9977-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="c9977-200">In VBScript wird die Fehlerbehandlung auch unter Verwendung des nativen **Err** -Objekts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9977-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="c9977-201">Sie können auch wie oben beschrieben auf das Objekt " [**taubemlasterror**](swbemlasterror.md)" zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c9977-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="c9977-202">Weitere Informationen finden Sie unter [Abrufen eines Fehlercodes](retrieving-an-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="c9977-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="c9977-203">Für PowerShell können Sie die Standardverfahren für die PowerShell-Fehlerbehandlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9977-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="c9977-204">Weitere Informationen finden Sie unter [Einführung in die Fehlerbehandlung in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="c9977-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
