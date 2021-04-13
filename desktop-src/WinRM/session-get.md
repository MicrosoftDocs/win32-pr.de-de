---
title: Session. Get-Methode (WSManDisp. h)
description: Ruft die vom URI angegebene Ressource ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Get-Methode Windows-Remoteverwaltung
- Get-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Get-Methode
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341018"
---
# <a name="sessionget-method"></a><span data-ttu-id="624c8-106">Session. Get-Methode</span><span class="sxs-lookup"><span data-stu-id="624c8-106">Session.Get method</span></span>

<span data-ttu-id="624c8-107">Ruft die vom [*URI*](windows-remote-management-glossary.md) angegebene Ressource ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="624c8-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="624c8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="624c8-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="624c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="624c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624c8-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="624c8-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="624c8-111">Der Bezeichner der abzurufenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="624c8-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="624c8-112">Dieser Parameter kann einen der folgenden Parameter enthalten:</span><span class="sxs-lookup"><span data-stu-id="624c8-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="624c8-113">Ein URI mit oder ohne [*Selektoren*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="624c8-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="624c8-114">Wenn Sie die **Get** -Methode mit einem Selektor aufrufen, um eine WMI-Ressource abzurufen, verwenden Sie die Schlüsseleigenschaft oder die Eigenschaften des Objekts.</span><span class="sxs-lookup"><span data-stu-id="624c8-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="624c8-115">Beispielsweise wird im folgenden Visual Basic Scripting Edition Codebeispiel (VBScript) der Schlüssel durch angegeben `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="624c8-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="624c8-116">Bei Singleton-Klassen, wie z. b. [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), kann kein Selektor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="624c8-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="624c8-117">Ein [**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="624c8-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="624c8-118">Ein [*WS-adressierungsend*](windows-remote-management-glossary.md) Punkt Verweis, wie im WS-Management Protocol-Standard beschrieben.</span><span class="sxs-lookup"><span data-stu-id="624c8-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="624c8-119">Weitere Informationen zur öffentlichen Spezifikation für [WS-Management-Protokoll](ws-management-protocol.md)finden Sie auf der [Seite Verwaltungs Spezifikationen Index](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="624c8-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="624c8-120">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="624c8-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="624c8-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="624c8-121">Reserved.</span></span> <span data-ttu-id="624c8-122">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="624c8-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="624c8-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="624c8-123">Return value</span></span>

<span data-ttu-id="624c8-124">Eine XML-Darstellung der Ressource.</span><span class="sxs-lookup"><span data-stu-id="624c8-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="624c8-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="624c8-125">Examples</span></span>

<span data-ttu-id="624c8-126">Im folgenden VBScript-Codebeispiel wird die XML-Darstellung der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Instanz abgerufen, die den WMI-WinMgmt-Dienst auf dem lokalen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="624c8-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


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


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



<span data-ttu-id="624c8-127">Im folgenden VBScript-Codebeispiel wird die WMI-WinMgmt-Dienst Instanz von einem Remote Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="624c8-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="624c8-128">Der Remote Computer wird durch den voll qualifizierten Domänen Namen (Servername.Domain.com) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="624c8-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="624c8-129">Der einzige Unterschied zwischen der lokalen Version und der Remote Version ist die Angabe des Remote Computers im [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen.</span><span class="sxs-lookup"><span data-stu-id="624c8-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



## <a name="requirements"></a><span data-ttu-id="624c8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="624c8-130">Requirements</span></span>



| <span data-ttu-id="624c8-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="624c8-131">Requirement</span></span> | <span data-ttu-id="624c8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="624c8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="624c8-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="624c8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="624c8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="624c8-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="624c8-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="624c8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="624c8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="624c8-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="624c8-137">Header</span><span class="sxs-lookup"><span data-stu-id="624c8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="624c8-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="624c8-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="624c8-139">IDL</span><span class="sxs-lookup"><span data-stu-id="624c8-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="624c8-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="624c8-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="624c8-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="624c8-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="624c8-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="624c8-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="624c8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="624c8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="624c8-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="624c8-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="624c8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="624c8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624c8-146">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="624c8-146">**Session**</span></span>](session.md)
</dt> </dl>

 

