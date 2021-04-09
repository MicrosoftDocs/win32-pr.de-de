---
title: Enumeratorobjekt (WSManDisp. h)
description: Stellt einen Stream von Ergebnissen dar, die von Vorgängen zurückgegeben werden, z. b. ein Pull
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- EnumeratorobjektWindows-Remoteverwaltung
- EnumeratorobjektWindows-Remoteverwaltung, beschrieben
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040926"
---
# <a name="enumerator-object"></a><span data-ttu-id="29154-105">Enumerator-Objekt</span><span class="sxs-lookup"><span data-stu-id="29154-105">Enumerator object</span></span>

<span data-ttu-id="29154-106">Stellt einen Stream von Ergebnissen dar, die von Vorgängen zurückgegeben werden, z. b. ein Pull</span><span class="sxs-lookup"><span data-stu-id="29154-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="29154-107">Beispielsweise gibt die [**Session. Enumerate**](session-enumerate.md) -Methode mehrere Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="29154-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="29154-108">Member</span><span class="sxs-lookup"><span data-stu-id="29154-108">Members</span></span>

<span data-ttu-id="29154-109">Das **Enumeratorobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="29154-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="29154-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="29154-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="29154-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29154-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="29154-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="29154-112">Methods</span></span>

<span data-ttu-id="29154-113">Das **Enumeratorobjekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="29154-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="29154-114">Methode</span><span class="sxs-lookup"><span data-stu-id="29154-114">Method</span></span>                                  | <span data-ttu-id="29154-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29154-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29154-116">**"ReadItem"**</span><span class="sxs-lookup"><span data-stu-id="29154-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="29154-117">Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="29154-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="29154-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29154-118">Properties</span></span>

<span data-ttu-id="29154-119">Das **Enumeratorobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29154-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="29154-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="29154-120">Property</span></span>                                                     | <span data-ttu-id="29154-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29154-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29154-122">**Atendof-Stream**</span><span class="sxs-lookup"><span data-stu-id="29154-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="29154-123">Ruft einen booleschen Wert ab, der angibt, ob in der Auflistung weitere Elemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="29154-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="29154-124">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="29154-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="29154-125">Ruft eine XML-Darstellung zusätzlicher Fehlerinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="29154-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="29154-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29154-126">Remarks</span></span>

<span data-ttu-id="29154-127">Verwenden Sie zum Starten einer Enumeration [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="29154-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="29154-128">Verwenden Sie zum Ausführen eines [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) -Vorgangs, der weiterhin Elemente in der-Enumeration liest, [**Enumerator. ReadItem**](enumerator-readitem.md).</span><span class="sxs-lookup"><span data-stu-id="29154-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="29154-129">Das **Enumeratorobjekt** entspricht der [**iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="29154-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="29154-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29154-130">Examples</span></span>

<span data-ttu-id="29154-131">Im folgenden VBScript-Codebeispiel werden alle Datenträger auf einem Remote Computer aufgelistet, die durch den voll qualifizierten Domänen Namen (Servername.Domain.com) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="29154-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="29154-132">Die DisplayOutput-Unterroutine formatiert die Datenausgabe auf die gleiche Weise wie das WinRM. cmd-Tool.</span><span class="sxs-lookup"><span data-stu-id="29154-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



## <a name="requirements"></a><span data-ttu-id="29154-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29154-133">Requirements</span></span>



| <span data-ttu-id="29154-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29154-134">Requirement</span></span> | <span data-ttu-id="29154-135">Wert</span><span class="sxs-lookup"><span data-stu-id="29154-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29154-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29154-136">Minimum supported client</span></span><br/> | <span data-ttu-id="29154-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29154-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="29154-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29154-138">Minimum supported server</span></span><br/> | <span data-ttu-id="29154-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29154-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="29154-140">Header</span><span class="sxs-lookup"><span data-stu-id="29154-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="29154-141"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="29154-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="29154-142">IDL</span><span class="sxs-lookup"><span data-stu-id="29154-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29154-143"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29154-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="29154-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29154-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="29154-145"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29154-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29154-146">DLL</span><span class="sxs-lookup"><span data-stu-id="29154-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29154-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29154-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29154-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29154-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29154-149">WinRM-Skript-API</span><span class="sxs-lookup"><span data-stu-id="29154-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="29154-150">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="29154-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="29154-151">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="29154-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





