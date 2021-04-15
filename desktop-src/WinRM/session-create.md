---
title: Session. Create-Methode (WSManDisp. h)
description: Erstellt eine neue Instanz einer Ressource und gibt den Endpunkt Verweis (EPR) des neuen-Objekts zurück.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Create-Methode Windows-Remoteverwaltung
- Create-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Create-Methode
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477685"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="7a623-106">Session. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="7a623-106">Session.Create method</span></span>

<span data-ttu-id="7a623-107">Erstellt eine neue Instanz einer Ressource und gibt den [*Endpunkt Verweis (EPR)*](windows-remote-management-glossary.md) des neuen-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="7a623-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a623-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a623-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7a623-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a623-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a623-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a623-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a623-111">Der Bezeichner der zu erstellenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="7a623-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="7a623-112">Dieser Parameter kann einen der folgenden Parameter enthalten:</span><span class="sxs-lookup"><span data-stu-id="7a623-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="7a623-113">Der URI mit mindestens einem [*Selektoren*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="7a623-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="7a623-114">Beachten Sie, dass das [*WMI-Plug-in*](windows-remote-management-glossary.md) das Erstellen einer anderen Ressource als einem [WS-Management-Protokoll](ws-management-protocol.md) Listener nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a623-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="7a623-115">[**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="7a623-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="7a623-116">Endpunkt Verweis der [*WS-Adressierung*](windows-remote-management-glossary.md) , wie im WS-Management Protocol-Standard beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7a623-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="7a623-117">Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Verwaltungs Spezifikationen Index page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7a623-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="7a623-118">*resource*</span><span class="sxs-lookup"><span data-stu-id="7a623-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="7a623-119">Der XML-Code, der Ressourcen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="7a623-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-120">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7a623-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a623-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="7a623-121">Reserved.</span></span> <span data-ttu-id="7a623-122">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a623-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a623-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a623-123">Return value</span></span>

<span data-ttu-id="7a623-124">Die EPR der neuen Ressource.</span><span class="sxs-lookup"><span data-stu-id="7a623-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a623-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a623-125">Remarks</span></span>

<span data-ttu-id="7a623-126">**Session. Create** wird nur zum Erstellen neuer Instanzen einer Ressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a623-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="7a623-127">Verwenden Sie die [**Session. Put**](session-put.md) -Methode, um vorhandene Instanzen einer Ressource zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7a623-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="7a623-128">Nachdem Sie den neuen Ressourcen-URI erhalten haben, können Sie [**Session. Get**](session-get.md) aufrufen, um das neue-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a623-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="7a623-129">Das neue-Objekt enthält alle Eigenschaften, die der Ressourcenanbieter beim Erstellen des neuen-Objekts zuweist.</span><span class="sxs-lookup"><span data-stu-id="7a623-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="7a623-130">Wenn Sie z. b. einen neuen [*WS-Management*](windows-remote-management-glossary.md) Protokolllistener erstellen und das Listenerobjekt mithilfe von **Session. Get** abrufen, erhalten Sie auch die Eigenschaften **Port**, **aktiviert** und **listeningon** .</span><span class="sxs-lookup"><span data-stu-id="7a623-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="7a623-131">Beachten Sie, dass das [*WMI-Plug-in*](windows-remote-management-glossary.md) keine Unterstützung für das Erstellen von Ressourcen bietet, die keine WS-Management Protokolllistener sind.</span><span class="sxs-lookup"><span data-stu-id="7a623-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="7a623-132">Die folgende Syntax wird verwendet, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a623-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="7a623-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a623-133">Examples</span></span>

<span data-ttu-id="7a623-134">Im folgenden VBScript-Codebeispiel wird **Session. Create** aufgerufen, um einen Listener auf dem lokalen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a623-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="7a623-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a623-135">Requirements</span></span>



| <span data-ttu-id="7a623-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a623-136">Requirement</span></span> | <span data-ttu-id="7a623-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7a623-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a623-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a623-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7a623-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a623-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7a623-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a623-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7a623-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a623-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7a623-142">Header</span><span class="sxs-lookup"><span data-stu-id="7a623-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a623-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a623-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a623-144">IDL</span><span class="sxs-lookup"><span data-stu-id="7a623-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a623-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a623-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7a623-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a623-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a623-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a623-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a623-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7a623-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a623-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a623-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a623-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a623-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a623-151">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="7a623-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="7a623-152">WS-Verwaltungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="7a623-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

