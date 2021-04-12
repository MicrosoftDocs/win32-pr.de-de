---
description: Die AuthenticationLevel-Eigenschaft ist eine ganze Zahl, die die com-Authentifizierungs Ebene definiert, die diesem Objekt zugewiesen ist.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Taubemsecurity. AuthenticationLevel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344709"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="d6221-103">Taubemsecurity. AuthenticationLevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6221-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="d6221-104">Die **AuthenticationLevel** -Eigenschaft ist eine ganze Zahl, die die com-Authentifizierungs Ebene definiert, die diesem Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d6221-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="d6221-105">Mit dieser Einstellung wird bestimmt, wie die von WMI gesendeten Informationen geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="d6221-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="d6221-106">Weitere Informationen zu Authentifizierungs Ebenen finden Sie unter [Festlegen der \_ \_ Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="d6221-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="d6221-107">Im Allgemeinen ist es nicht notwendig, die Authentifizierungs Ebene beim Ausführen von WMI-API-aufrufen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d6221-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="d6221-108">Wenn Sie diese Eigenschaft nicht festlegen, wird die Standard-com-Authentifizierungs Ebene für das System verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6221-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="d6221-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d6221-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d6221-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d6221-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6221-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6221-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="d6221-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d6221-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d6221-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6221-113">Remarks</span></span>

<span data-ttu-id="d6221-114">Mithilfe der AuthenticationLevel-Einstellung können Sie die Ebene der DCOM-Authentifizierung und des Datenschutzes anfordern, die während der gesamten Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6221-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="d6221-115">Die Einstellungen reichen von der Authentifizierung über die verschlüsselte Authentifizierung per Paket.</span><span class="sxs-lookup"><span data-stu-id="d6221-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="d6221-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d6221-116">Value</span></span>        | <span data-ttu-id="d6221-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6221-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6221-118">Keine</span><span class="sxs-lookup"><span data-stu-id="d6221-118">None</span></span>         | <span data-ttu-id="d6221-119">Verwendet keine Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="d6221-119">Does not use any authentication.</span></span> <span data-ttu-id="d6221-120">Alle Sicherheitseinstellungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d6221-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="d6221-121">Standard</span><span class="sxs-lookup"><span data-stu-id="d6221-121">Default</span></span>      | <span data-ttu-id="d6221-122">Verwendet eine Standard-Sicherheitsaus Handlung, um eine Authentifizierungs Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d6221-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="d6221-123">Dies ist die empfohlene Einstellung, da der an der Transaktion beteiligte Client mit der vom Server angegebenen Authentifizierungs Ebene ausgehandelt wird.</span><span class="sxs-lookup"><span data-stu-id="d6221-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="d6221-124">Der Wert None während einer Aushandlungs Sitzung wird von DCOM nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d6221-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="d6221-125">Verbinden</span><span class="sxs-lookup"><span data-stu-id="d6221-125">Connect</span></span>      | <span data-ttu-id="d6221-126">Authentifiziert die Anmelde Informationen des Clients nur, wenn der Client versucht, eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="d6221-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="d6221-127">Nachdem eine Verbindung hergestellt wurde, werden keine weiteren Authentifizierungsprüfungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6221-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="d6221-128">Aufruf</span><span class="sxs-lookup"><span data-stu-id="d6221-128">Call</span></span>         | <span data-ttu-id="d6221-129">Authentifiziert die Anmelde Informationen des Clients nur zu Beginn jedes Aufrufes, wenn der Server die Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="d6221-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="d6221-130">Die Paket Header sind signiert, aber die zwischen Client und Server ausgetauschten Datenpakete sind weder signiert noch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d6221-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="d6221-131">Pkt</span><span class="sxs-lookup"><span data-stu-id="d6221-131">Pkt</span></span>          | <span data-ttu-id="d6221-132">Authentifiziert, dass alle Datenpakete vom erwarteten Client empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="d6221-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="d6221-133">Vergleichbar mit "Call;" Paket Header sind signiert, aber nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d6221-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="d6221-134">Pakete selbst sind weder signiert noch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d6221-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="d6221-135">PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="d6221-135">PktIntegrity</span></span> | <span data-ttu-id="d6221-136">Authentifiziert und überprüft, ob keines der Datenpakete, die zwischen dem Client und dem Server übertragen wurden, geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d6221-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="d6221-137">Jedes Datenpaket wird signiert und stellt sicher, dass die Pakete während der Übertragung nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="d6221-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="d6221-138">Keines der Datenpakete ist verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d6221-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="d6221-139">PKTPRIVACY</span><span class="sxs-lookup"><span data-stu-id="d6221-139">PktPrivacy</span></span>   | <span data-ttu-id="d6221-140">Authentifiziert alle vorherigen Identitätswechsel Ebenen und signiert und verschlüsselt jedes Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="d6221-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="d6221-141">Dadurch wird sichergestellt, dass die gesamte Kommunikation zwischen dem Client und dem Server vertraulich ist.</span><span class="sxs-lookup"><span data-stu-id="d6221-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="d6221-142">Sie können die Authentifizierungs Ebene der Objekte " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbewbjectset**](swbemobjectset.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**taubemlocator**](swbemlocator.md) " festlegen, indem Sie die Eigenschaft " **AuthenticationLevel** " auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6221-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="d6221-143">Im folgenden Beispiel wird gezeigt, wie Sie die Authentifizierungs Ebene für ein " **errbemubject** "-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6221-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="d6221-144">Sie können auch Authentifizierungs Ebenen als Teil eines Monikers angeben.</span><span class="sxs-lookup"><span data-stu-id="d6221-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="d6221-145">Im folgenden Beispiel werden die Authentifizierungs Ebene und die Identitätswechsel Ebene festgelegt, und es wird eine Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d6221-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="d6221-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6221-146">Requirements</span></span>



| <span data-ttu-id="d6221-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6221-147">Requirement</span></span> | <span data-ttu-id="d6221-148">Wert</span><span class="sxs-lookup"><span data-stu-id="d6221-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6221-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6221-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d6221-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6221-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6221-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6221-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d6221-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6221-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6221-153">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d6221-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6221-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6221-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6221-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d6221-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6221-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6221-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6221-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="d6221-157">CLSID</span></span><br/>                    | <span data-ttu-id="d6221-158">CLSID- \_ Swap-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d6221-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="d6221-159">IID</span><span class="sxs-lookup"><span data-stu-id="d6221-159">IID</span></span><br/>                      | <span data-ttu-id="d6221-160">IID \_ iswbemsecurity</span><span class="sxs-lookup"><span data-stu-id="d6221-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d6221-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6221-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6221-162">Festlegen der \_ Prozesssicherheit für Client Anwendungen \_</span><span class="sxs-lookup"><span data-stu-id="d6221-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="d6221-163">**Wbemauthenticationlevelerum**</span><span class="sxs-lookup"><span data-stu-id="d6221-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="d6221-164">**Austausch Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="d6221-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

