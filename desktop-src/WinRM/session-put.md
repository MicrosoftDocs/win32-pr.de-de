---
title: Session. Put-Methode (WSManDisp. h)
description: Aktualisieren Sie eine Ressource.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put-Methode Windows-Remoteverwaltung
- Put-Methode Windows-Remoteverwaltung, Session-Objekt
- Session-Objekt Windows-Remoteverwaltung, Put-Methode
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392057"
---
# <a name="sessionput-method"></a><span data-ttu-id="599fd-106">Session. Put-Methode</span><span class="sxs-lookup"><span data-stu-id="599fd-106">Session.Put method</span></span>

<span data-ttu-id="599fd-107">Aktualisieren Sie eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="599fd-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="599fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="599fd-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="599fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="599fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="599fd-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="599fd-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="599fd-111">Der Bezeichner der zu aktualisierenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="599fd-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="599fd-112">Dieser Parameter kann eines der-Elemente enthalten, die in der folgenden Liste enthalten sind:</span><span class="sxs-lookup"><span data-stu-id="599fd-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="599fd-113">URI mit oder ohne [*Selektoren*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="599fd-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="599fd-114">Wenn Sie die **Put** -Methode aufrufen, um eine WMI-Ressource abzurufen, verwenden Sie die Schlüsseleigenschaft oder die Eigenschaften des Objekts.</span><span class="sxs-lookup"><span data-stu-id="599fd-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="599fd-115">Beispielsweise wird im folgenden Visual Basic Scripting Edition Codebeispiel (VBScript) der Schlüssel durch angegeben `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="599fd-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="599fd-116">[**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="599fd-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="599fd-117">Endpunkt Verweis der [*WS-Adressierung*](windows-remote-management-glossary.md) , wie im [WS-Management-Protokoll](ws-management-protocol.md) -Standard beschrieben.</span><span class="sxs-lookup"><span data-stu-id="599fd-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="599fd-118">Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Verwaltungs Spezifikationen Index page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="599fd-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="599fd-119">*Ressource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="599fd-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="599fd-120">Der aktualisierte Ressourcen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="599fd-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="599fd-121">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="599fd-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="599fd-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="599fd-122">Reserved.</span></span> <span data-ttu-id="599fd-123">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="599fd-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="599fd-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="599fd-124">Return value</span></span>

<span data-ttu-id="599fd-125">Der XML-Code, der den aktualisierten Ressourcen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="599fd-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="599fd-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="599fd-126">Examples</span></span>

<span data-ttu-id="599fd-127">Im folgenden VBScript-Codebeispiel werden Daten in das [**Win32- \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) -Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="599fd-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="599fd-128">Sie müssen alle nicht-Array-Eigenschaften des-Objekts in der XML-Datei des *Ressourcen* Parameters einschließen.</span><span class="sxs-lookup"><span data-stu-id="599fd-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="599fd-129">Die Reihenfolge der Eigenschaften ist nicht signifikant.</span><span class="sxs-lookup"><span data-stu-id="599fd-129">The order of the properties is not significant.</span></span>


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a><span data-ttu-id="599fd-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="599fd-130">Requirements</span></span>



| <span data-ttu-id="599fd-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="599fd-131">Requirement</span></span> | <span data-ttu-id="599fd-132">Wert</span><span class="sxs-lookup"><span data-stu-id="599fd-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="599fd-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="599fd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="599fd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="599fd-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="599fd-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="599fd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="599fd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="599fd-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="599fd-137">Header</span><span class="sxs-lookup"><span data-stu-id="599fd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="599fd-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="599fd-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="599fd-139">IDL</span><span class="sxs-lookup"><span data-stu-id="599fd-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="599fd-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="599fd-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="599fd-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="599fd-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="599fd-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="599fd-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="599fd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="599fd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599fd-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599fd-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="599fd-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="599fd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599fd-146">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="599fd-146">**Session**</span></span>](session.md)
</dt> </dl>

 

