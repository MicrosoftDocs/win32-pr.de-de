---
title: ResourceLocator-Objekt (WSManDisp. h)
description: Gibt den Pfad zu einer Ressource an. Sie können ein ResourceLocator-Objekt anstelle eines Ressourcen-URI in Sitzungs Objekt Vorgängen verwenden, z. b. "Session. Get", "Session. Put" oder "Session. Enumerate".
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- ResourceLocator-Objekt Windows-Remoteverwaltung
- ResourceLocator-Objekt Windows-Remoteverwaltung, beschrieben
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103078"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="a5d4c-106">ResourceLocator-Objekt</span><span class="sxs-lookup"><span data-stu-id="a5d4c-106">ResourceLocator object</span></span>

<span data-ttu-id="a5d4c-107">Ein-Objekt, das den Pfad zu einer Ressource bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="a5d4c-108">Sie können ein **ResourceLocator** -Objekt anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwenden, z. b. " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)".</span><span class="sxs-lookup"><span data-stu-id="a5d4c-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="a5d4c-109">Mit diesem Objekt können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="a5d4c-109">This object enables you to:</span></span>

-   <span data-ttu-id="a5d4c-110">Fügen Sie mindestens einen [*Selektoren*](windows-remote-management-glossary.md) hinzu, der eine bestimmte Instanz einer Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="a5d4c-111">Dies entspricht dem Angeben eines Schlüssel Werts im Ressourcen-URI für eine Ressource, die Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="a5d4c-112">Weitere Informationen finden Sie unter [**ResourceLocator. addselector**](resourcelocator-addselector.md).</span><span class="sxs-lookup"><span data-stu-id="a5d4c-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="a5d4c-113">Sie können einen ähnlichen Vorgang ausführen, indem Sie den *Filter* -Parameter in einem Aufrufen von [**Session. Enumerate**](session-enumerate.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="a5d4c-114">Geben Sie einen [*Fragmentpfad*](windows-remote-management-glossary.md) und einen Dialekt an, um nur eine Eigenschaft einer Ressource zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="a5d4c-115">Sie können auch ein oder alle Elemente einer Array Eigenschaft angeben, indem Sie den Array Index bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="a5d4c-116">Weitere Informationen finden Sie unter [**ResourceLocator. fragmentpath**](resourcelocator-fragmentpath.md).</span><span class="sxs-lookup"><span data-stu-id="a5d4c-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="a5d4c-117">Fügen Sie eine oder mehrere [*Optionen*](windows-remote-management-glossary.md) hinzu, die eine Datenquelle möglicherweise benötigt, um eine Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="a5d4c-118">Weitere Informationen finden Sie unter [**ResourceLocator. AddOption**](resourcelocator-addoption.md).</span><span class="sxs-lookup"><span data-stu-id="a5d4c-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="a5d4c-119">Weitere Informationen finden Sie unter [Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="a5d4c-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="a5d4c-120">Member</span><span class="sxs-lookup"><span data-stu-id="a5d4c-120">Members</span></span>

<span data-ttu-id="a5d4c-121">Das **ResourceLocator** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a5d4c-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="a5d4c-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="a5d4c-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="a5d4c-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5d4c-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a5d4c-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="a5d4c-124">Methods</span></span>

<span data-ttu-id="a5d4c-125">Das **ResourceLocator** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="a5d4c-126">Methode</span><span class="sxs-lookup"><span data-stu-id="a5d4c-126">Method</span></span>                                                   | <span data-ttu-id="a5d4c-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5d4c-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5d4c-128">**AddOption**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="a5d4c-129">Fügt zusätzliche Daten hinzu, die für die Verarbeitung der Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="a5d4c-130">**Addselector**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="a5d4c-131">Fügt dem **ResourceLocator** -Objekt einen [*Selektor*](windows-remote-management-glossary.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="a5d4c-132">**Clearoptions**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="a5d4c-133">Entfernt alle [*Optionen*](windows-remote-management-glossary.md) aus dem **ResourceLocator** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="a5d4c-134">**Clearselectors**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="a5d4c-135">Entfernt alle Selektoren aus einem **ResourceLocator** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="a5d4c-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5d4c-136">Properties</span></span>

<span data-ttu-id="a5d4c-137">Das **ResourceLocator** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="a5d4c-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a5d4c-138">Property</span></span>                                                                          | <span data-ttu-id="a5d4c-139">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a5d4c-139">Access type</span></span>           | <span data-ttu-id="a5d4c-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5d4c-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5d4c-141">**Fragmentdialekt**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="a5d4c-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5d4c-142">Read/write</span></span><br/> | <span data-ttu-id="a5d4c-143">Ruft den sprach Dialekt für ein [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md)ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="a5d4c-144">**Fragmentpath**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="a5d4c-145">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5d4c-145">Read/write</span></span><br/> | <span data-ttu-id="a5d4c-146">Ruft den Pfad für ein [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md) oder eine Ressourcen Eigenschaft ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="a5d4c-147">**Mustverständlicherweise-Optionen**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="a5d4c-148">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5d4c-148">Read/write</span></span><br/> | <span data-ttu-id="a5d4c-149">Ruft den **mustverständlicherweise Options** -Wert für das **ResourceLocator** -Objekt ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a5d4c-150">**ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="a5d4c-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="a5d4c-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5d4c-151">Read/write</span></span><br/> | <span data-ttu-id="a5d4c-152">Ruft den Ressourcen- [*URI*](windows-remote-management-glossary.md) in einem **ResourceLocator** -Objekt ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="a5d4c-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5d4c-153">Remarks</span></span>

<span data-ttu-id="a5d4c-154">Das **ResourceLocator** -Objekt entspricht der **iwsmanresourcelocator** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="a5d4c-155">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5d4c-155">Examples</span></span>

<span data-ttu-id="a5d4c-156">Im folgenden VBScript-Codebeispiel werden die Eigenschaften " **numoflogicalprocessor** " und " **numofcores** " von einer bestimmten Instanz des [**Win32- \_ Prozessors**](/windows/desktop/CIMWin32Prov/win32-processor)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5d4c-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a5d4c-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5d4c-157">Requirements</span></span>



| <span data-ttu-id="a5d4c-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5d4c-158">Requirement</span></span> | <span data-ttu-id="a5d4c-159">Wert</span><span class="sxs-lookup"><span data-stu-id="a5d4c-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d4c-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5d4c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d4c-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5d4c-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a5d4c-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5d4c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d4c-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5d4c-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a5d4c-164">Header</span><span class="sxs-lookup"><span data-stu-id="a5d4c-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d4c-165"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d4c-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5d4c-166">IDL</span><span class="sxs-lookup"><span data-stu-id="a5d4c-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5d4c-167"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5d4c-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a5d4c-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5d4c-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5d4c-169"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5d4c-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a5d4c-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a5d4c-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d4c-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5d4c-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5d4c-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5d4c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d4c-173">WinRM-Skript-API</span><span class="sxs-lookup"><span data-stu-id="a5d4c-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

