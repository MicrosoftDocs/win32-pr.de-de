---
description: Gelegentlich kann es vorkommen, dass Sie nur einen Teil einer Instanz aktualisieren möchten.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Aktualisieren eines Teils einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372949"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="c2845-103">Aktualisieren eines Teils einer Instanz</span><span class="sxs-lookup"><span data-stu-id="c2845-103">Updating Part of an Instance</span></span>

<span data-ttu-id="c2845-104">Gelegentlich kann es vorkommen, dass Sie nur einen Teil einer Instanz aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c2845-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="c2845-105">Einige Instanzen verfügen z. b. über eine große Anzahl von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2845-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="c2845-106">Wenn Sie eine große Anzahl dieser Instanzen aktualisieren müssen, können Sie die Systemleistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c2845-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="c2845-107">Aus diesem Grund können Sie auswählen, dass nur ein Teil der-Instanz aktualisiert wird, und so die Menge an Informationen reduzieren, die Sie an und von WMI senden und abrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="c2845-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="c2845-108">Allerdings unterstützt WMI nicht direkt Vorgänge für partielle Instanzen oder die meisten Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c2845-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="c2845-109">Wenn Sie also eine Anwendung schreiben, die partielle instanzvorgänge verwendet, sollten Sie darauf vorbereitet sein, dass Ihre Aufrufe fehlschlagen, wenn der **WBEM \_ e- \_ Anbieter \_ nicht \_** unterstützt oder der Fehlercode **WBEM \_ e \_ nicht \_ unterstützt** in C++ ist.</span><span class="sxs-lookup"><span data-stu-id="c2845-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="c2845-110">In Skriptsprachen sind die Fehlercodes entweder **wbemErrProviderNotCapable** oder **wbemErrNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="c2845-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="c2845-111">Bei der Skripterstellung ist dieser Vorgang nur erforderlich, um die Leistung beim Aktualisieren von einer oder zwei beschreibbaren Eigenschaften in einer sehr großen Anzahl von Objekten über ein Unternehmen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c2845-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="c2845-112">Andernfalls aktualisieren die normalen VBScript-Aufrufe von " [**errbewbject \_ . Put**](swbemobject-put-.md) " oder " [**errbejebject \_ . putasync**](swbemobject-putasync-.md)", während Sie das gesamte Objekt schreiben, tatsächlich nur die Eigenschaften aktualisieren, für die der Anbieter Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="c2845-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="c2845-113">Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von PowerShell ein partielles instanzupdate anfordern.</span><span class="sxs-lookup"><span data-stu-id="c2845-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="c2845-114">**So fordern Sie eine teilinstanzaktualisierung mithilfe von PowerShell an**</span><span class="sxs-lookup"><span data-stu-id="c2845-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="c2845-115">Rufen Sie den Pfad des Objekts ab, das Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c2845-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="c2845-116">Sie können den Pfad entweder manuell beschreiben oder das Objekt Abfragen und dann die **\_ \_ path** -Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="c2845-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="c2845-117">Richten Sie eine Hash Tabelle ein, die die Namen der zu aktualisierenden Eigenschaften auflistet, und verwenden Sie diese Hash Tabelle in einem-Befehl von [Set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="c2845-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="c2845-118">Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von c# eine partielle Instanzaktualisierung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c2845-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="c2845-119">**System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.</span><span class="sxs-lookup"><span data-stu-id="c2845-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="c2845-120">**So fordern Sie eine teilinstanzaktualisierung mithilfe von C an #**</span><span class="sxs-lookup"><span data-stu-id="c2845-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="c2845-121">Erstellen Sie ein neues [Management Object](/dotnet/api/system.management.managementobject) -Objekt, das die zu Aktualisier gende Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2845-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="c2845-122">Legen Sie den Eigenschafts Wert mit einem Aufrufen von [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_)fest.</span><span class="sxs-lookup"><span data-stu-id="c2845-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="c2845-123">Im folgenden Verfahren wird beschrieben, wie Sie mit VBScript eine partielle Instanzaktualisierung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c2845-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="c2845-124">**So fordern Sie eine teilinstanzaktualisierung mithilfe von VBScript an**</span><span class="sxs-lookup"><span data-stu-id="c2845-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="c2845-125">Erstellen Sie ein [**Swap**](swbemnamedvalueset.md) -Kontext Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2845-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="c2845-126">Fügen Sie die Put-Erweiterungs Werte " \_ \_ Put \_ Extensions" und " \_ \_ Put \_ Ext \_ Client \_ Request" dem Kontext Objekt mithilfe der Methode " [**Swap Name. Add**](swbemnamedvalueset-add.md) " hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2845-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="c2845-127">Richten Sie ein Array ein, das die Namen der zu aktualisierenden Eigenschaften auflistet, [](swbemnamedvalueset.md) und fügen Sie das Array mit dem Wert der Put-Erweiterung " \_ \_ Put \_ Ext \_ Properties" dem Kontext Objekt "Swap Name" hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2845-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="c2845-128">Legen Sie den *IFlags* -Parameter des Austauschs "WS- [**imbject. Put \_**](swbemobject-put-.md) " auf " **wbemchangeflagupdateonly**" fest.</span><span class="sxs-lookup"><span data-stu-id="c2845-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="c2845-129">Ohne dieses Flag schlägt der-Befehl mit einem ungültigen Kontext fehl.</span><span class="sxs-lookup"><span data-stu-id="c2845-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="c2845-130">Übergeben Sie Ihr Flag und das Kontext Objekt an den Anbieter in den *objwbemnamedvalueset* -Parametern von " [**errbefubject. Put \_**](swbemobject-put-.md) " oder " [**Swap. putasync \_**](swbemobject-putasync-.md)".</span><span class="sxs-lookup"><span data-stu-id="c2845-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="c2845-131">Im folgenden Verfahren wird beschrieben, wie Sie eine teilinstanzaktualisierung mithilfe von C++ anfordern.</span><span class="sxs-lookup"><span data-stu-id="c2845-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="c2845-132">**So fordern Sie eine teilinstanzaktualisierung mithilfe von C++ an**</span><span class="sxs-lookup"><span data-stu-id="c2845-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="c2845-133">Erstellen Sie ein [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c2845-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="c2845-134">Ein Kontext Objekt ist ein Objekt, das WMI verwendet, um weitere Informationen an einen WMI-Anbieter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c2845-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="c2845-135">In diesem Fall verwenden Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt, um den Anbieter anzuweisen, partielle instanzaktualisierungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="c2845-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="c2845-136">Fügen Sie die \_ \_ \_ benannten Werte "Put Extensions" und " \_ \_ Put \_ Ext \_ Client \_ Request" zum [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt hinzu, indem Sie " [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c2845-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="c2845-137">In der folgenden Tabelle sind die Bedeutung von " \_ \_ Put \_ Extensions" und " \_ \_ Put \_ Ext \_ Client \_ Request" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2845-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="c2845-138">Benannter Wert</span><span class="sxs-lookup"><span data-stu-id="c2845-138">Named value</span></span>                     | <span data-ttu-id="c2845-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2845-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c2845-140">" \_ \_ Put \_ Extensions"</span><span class="sxs-lookup"><span data-stu-id="c2845-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="c2845-141">**VT \_ Bool** auf **Variant \_ true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2845-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c2845-142">Ein-Wert, der angibt, dass ein oder mehrere der anderen Kontext Werte angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="c2845-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="c2845-143">Dies ermöglicht eine schnelle Überprüfung des Kontext Objekts innerhalb des Anbieters, um zu bestimmen, ob Updates für Teil Instanzen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2845-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="c2845-144">" \_ \_ \_ Ext- \_ Client \_ Anforderung ablegen"</span><span class="sxs-lookup"><span data-stu-id="c2845-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="c2845-145">**VT \_ Bool** auf **Variant \_ true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2845-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c2845-146">Wird vom Client während der anfänglichen Anforderung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2845-146">Set by the client during the initial request.</span></span> <span data-ttu-id="c2845-147">Dieser Wert wird verwendet, um Fehler beim erneuten eintreten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c2845-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="c2845-148">Fügen Sie die " \_ \_ Put \_ ext Strict NULLS"-Eigenschaft, "Put ext"-Eigenschaften oder "Set Ext \_ \_ \_ \_ \_ Atomic" \_ \_ \_ \_ \_ in beliebiger Kombination für das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt mit einem weiteren [**callbemcontext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)-Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2845-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="c2845-149">In der folgenden Tabelle wird die Bedeutung der benannten Werte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c2845-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="c2845-150">Benannter Wert</span><span class="sxs-lookup"><span data-stu-id="c2845-150">Named value</span></span>                   | <span data-ttu-id="c2845-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2845-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c2845-152">" \_ \_ Put \_ Ext \_ Strict \_ NULLS"</span><span class="sxs-lookup"><span data-stu-id="c2845-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="c2845-153">**VT \_ Bool** auf **Variant \_ true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2845-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c2845-154">Gibt an, dass der Client die Eigenschaften absichtlich auf **VT \_ null** festgelegt hat und erwartet, dass der Schreibvorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c2845-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="c2845-155">Wenn der Anbieter die Werte nicht auf **null** festlegen kann, sollte ein Fehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="c2845-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="c2845-156">" \_ \_ Put \_ Ext- \_ Eigenschaften"</span><span class="sxs-lookup"><span data-stu-id="c2845-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="c2845-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Zeichen folgen, die eine Liste der zu aktualisierenden Eigenschaften Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2845-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="c2845-158">Kann allein oder in Kombination mit " \_ \_ Put \_ Ext \_ Properties" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2845-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="c2845-159">Die Werte befinden sich in der-Instanz, die geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c2845-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="c2845-160">" \_ \_ Put \_ Ext \_ Atomic"</span><span class="sxs-lookup"><span data-stu-id="c2845-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="c2845-161">**VT \_ Bool** auf **Variant \_ true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2845-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c2845-162">Gibt an, dass alle Updates gleichzeitig ausgeführt werden müssen (atomarische Semantik), oder der Anbieter muss rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="c2845-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="c2845-163">Es kann kein Teilerfolg geben.</span><span class="sxs-lookup"><span data-stu-id="c2845-163">There can be no partial success.</span></span> <span data-ttu-id="c2845-164">Kann allein oder in Kombination mit anderen Flags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2845-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="c2845-165">Legen Sie den *IFlags* -Parameter auf das **WBEM- \_ Flag \_ \_ nur aktualisieren** fest.</span><span class="sxs-lookup"><span data-stu-id="c2845-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="c2845-166">Ohne dieses Flag schlägt der-Befehl mit einem ungültigen Kontext fehl.</span><span class="sxs-lookup"><span data-stu-id="c2845-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="c2845-167">Übergeben Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Kontext Objekt in beliebige Aufrufe [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) im *pctX* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c2845-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="c2845-168">Wenn Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt übergeben, weist der Anbieter an, partielle instanzaktualisierungen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="c2845-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="c2845-169">Bei einem vollständigen instanzupdate legen Sie *pctX* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="c2845-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="c2845-170">Der Anbieter kann alle notwendigen Eigenschaften schreiben, wenn das im-Befehl vorhandene Kontext Objekt keine " \_ \_ Put \_ Extensions" enthält.</span><span class="sxs-lookup"><span data-stu-id="c2845-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="c2845-171">Wenn " \_ \_ Put \_ Extensions" im Context-Objekt vorhanden ist, erfordert WMI, dass der Anbieter die Semantik des Vorgangs genau befolgt oder der-Befehl andernfalls fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c2845-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="c2845-172">Weitere Informationen finden Sie unter [Behandeln von Zugriffen auf Abgelehnte Nachrichten in einem Anbieter](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c2845-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
