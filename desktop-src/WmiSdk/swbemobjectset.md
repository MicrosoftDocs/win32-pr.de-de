---
description: Ein errbemubjectset-Objekt ist eine Auflistung von Swap-Objekten. Weitere Informationen finden Sie unter Zugreifen auf eine Sammlung. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Errbemubjectset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218294"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="8372b-105">Errbemubjectset-Objekt</span><span class="sxs-lookup"><span data-stu-id="8372b-105">SWbemObjectSet object</span></span>

<span data-ttu-id="8372b-106">Ein **errbemubjectset** -Objekt ist eine Auflistung von [**Swap**](swbemobject.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="8372b-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="8372b-107">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="8372b-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="8372b-108">Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8372b-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="8372b-109">Sie können ein Objekt von " **errbemubjectset** " abrufen, indem Sie eine der folgenden Methoden oder deren asynchrone Entsprechungen aufrufen:</span><span class="sxs-lookup"><span data-stu-id="8372b-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="8372b-110">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="8372b-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="8372b-111">**"Errbemubject. Instance"\_**</span><span class="sxs-lookup"><span data-stu-id="8372b-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="8372b-112">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="8372b-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="8372b-113">**Swap. subclasses\_**</span><span class="sxs-lookup"><span data-stu-id="8372b-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="8372b-114">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="8372b-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="8372b-115">**CquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="8372b-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="8372b-116">**Swap Services. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="8372b-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="8372b-117">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="8372b-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="8372b-118">**Swap Services. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="8372b-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="8372b-119">Das Objekt " **errbemubjectset** " unterstützt die optionalen **Add** -und **Remove** -Auflistungs Methoden nicht.</span><span class="sxs-lookup"><span data-stu-id="8372b-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="8372b-120">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, empfiehlt es sich, anstelle der asynchronen Kommunikation semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8372b-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="8372b-121">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8372b-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="8372b-122">Member</span><span class="sxs-lookup"><span data-stu-id="8372b-122">Members</span></span>

<span data-ttu-id="8372b-123">Das " **errbeporbjectset** "-Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8372b-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="8372b-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="8372b-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="8372b-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8372b-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8372b-126">Methoden</span><span class="sxs-lookup"><span data-stu-id="8372b-126">Methods</span></span>

<span data-ttu-id="8372b-127">Das Objekt " **errbemubjectset** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8372b-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="8372b-128">Methode</span><span class="sxs-lookup"><span data-stu-id="8372b-128">Method</span></span>                              | <span data-ttu-id="8372b-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8372b-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8372b-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="8372b-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="8372b-131">Ruft [**ein-**](swbemobject.md) Objekt aus der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="8372b-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="8372b-132">Dies ist die Standardmethode des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8372b-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8372b-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8372b-133">Properties</span></span>

<span data-ttu-id="8372b-134">Das Objekt " **errbemubjectset** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8372b-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="8372b-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8372b-135">Property</span></span>                                                  | <span data-ttu-id="8372b-136">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8372b-136">Access type</span></span>          | <span data-ttu-id="8372b-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8372b-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="8372b-138">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="8372b-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="8372b-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8372b-139">Read-only</span></span><br/> | <span data-ttu-id="8372b-140">Die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="8372b-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="8372b-141">**Sicherheit\_**</span><span class="sxs-lookup"><span data-stu-id="8372b-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="8372b-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8372b-142">Read-only</span></span><br/> | <span data-ttu-id="8372b-143">Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8372b-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8372b-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8372b-144">Remarks</span></span>

<span data-ttu-id="8372b-145">Ein " **errbemubjectset** " ist eine Auflistung von 0 (null) oder mehr " [**errbejebject**](swbemobject.md) "-Objekten.</span><span class="sxs-lookup"><span data-stu-id="8372b-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="8372b-146">Jedes "Swap"- **Objekt** in einem " **errbemubjectset** " kann eine der beiden folgenden Punkte darstellen:</span><span class="sxs-lookup"><span data-stu-id="8372b-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="8372b-147">Eine Instanz einer von WMI verwalteten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8372b-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="8372b-148">Eine Instanz einer Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="8372b-148">An instance of a class definition.</span></span>

<span data-ttu-id="8372b-149">Diese Klasse wird am häufigsten in WMI als Rückgabewert für einen [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) -oder [**InstancesOf**](swbemservices-instancesof.md) -Rückruf verwendet, wie im folgenden Codebeispiel beschrieben:</span><span class="sxs-lookup"><span data-stu-id="8372b-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="8372b-150">Der einzige Schritt, den Sie jemals mit einem " **errbemubjectset** " ausführen, ist das Auflisten aller Objekte, die in der Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8372b-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="8372b-151">Allerdings enthält " **errbewbjectset** " eine Eigenschaften Anzahl, die bei der Skripterstellung für die System Administration nützlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="8372b-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="8372b-152">Wie der Name schon sagt, gibt count die Anzahl der Elemente in der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="8372b-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="8372b-153">Dieses Skript ruft z. b. eine Sammlung aller auf einem Computer installierten Dienste ab und gibt dann die Gesamtzahl der gefundenen Dienste wieder:</span><span class="sxs-lookup"><span data-stu-id="8372b-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="8372b-154">Weitere Informationen zur Verwendung dieser Klasse finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="8372b-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8372b-155">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8372b-155">Examples</span></span>

<span data-ttu-id="8372b-156">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie die Austausch Vorgänge von " **errbewbjectset** " manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="8372b-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="8372b-157">Im folgenden perl-Codebeispiel wird veranschaulicht, wie die **Swap-Auflistungen von Swap**</span><span class="sxs-lookup"><span data-stu-id="8372b-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="8372b-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8372b-158">Requirements</span></span>



| <span data-ttu-id="8372b-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8372b-159">Requirement</span></span> | <span data-ttu-id="8372b-160">Wert</span><span class="sxs-lookup"><span data-stu-id="8372b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8372b-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8372b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8372b-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8372b-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8372b-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8372b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8372b-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8372b-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8372b-165">Header</span><span class="sxs-lookup"><span data-stu-id="8372b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="8372b-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8372b-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8372b-167">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8372b-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="8372b-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8372b-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8372b-169">DLL</span><span class="sxs-lookup"><span data-stu-id="8372b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8372b-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8372b-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8372b-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="8372b-171">CLSID</span></span><br/>                    | <span data-ttu-id="8372b-172">CLSID- \_ Swap-Objekt Satz</span><span class="sxs-lookup"><span data-stu-id="8372b-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="8372b-173">IID</span><span class="sxs-lookup"><span data-stu-id="8372b-173">IID</span></span><br/>                      | <span data-ttu-id="8372b-174">IID \_ iswbemubjectset</span><span class="sxs-lookup"><span data-stu-id="8372b-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="8372b-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8372b-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8372b-176">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="8372b-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




