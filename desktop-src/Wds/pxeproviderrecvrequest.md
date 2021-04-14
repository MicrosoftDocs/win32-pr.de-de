---
title: Pxeproviderrecvrequest-Rückruffunktion
description: Wird aufgerufen, wenn eine Anforderung von einem Client empfangen wird.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Pxeproviderrecvrequest-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391915"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="277c6-104">Pxeproviderrecvrequest-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="277c6-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="277c6-105">Wird aufgerufen, wenn eine Anforderung von einem Client empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="277c6-105">Called when a request is received from a client.</span></span> <span data-ttu-id="277c6-106">Diese Funktion wird durch Aufrufen der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert, wobei der *CallbackType* -Parameter auf **PXE \_ Callback \_ recv \_ Request** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="277c6-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="277c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="277c6-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="277c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="277c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277c6-109">*hclientrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277c6-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-110">Handle für eine Anforderung, die von einem Client empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="277c6-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="277c6-111">*ppacket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277c6-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-112">Zeiger auf den Arbeitsspeicher Puffer, der das empfangene Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="277c6-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="277c6-113">*upacketlen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277c6-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-114">Länge (in Byte) des Puffers, auf den der *ppacket* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="277c6-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="277c6-115">*plocaladdress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277c6-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-116">Zeiger auf eine [**PXE- \_ Adress**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) Struktur, die die lokale Adresse enthält, an der das Paket empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="277c6-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="277c6-117">*prämoteaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277c6-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-118">Zeiger auf eine [**PXE- \_ Adress**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) Struktur, die die Quelladresse des Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="277c6-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="277c6-119">*pAction* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="277c6-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-120">Gibt die Aktion an, die das System ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="277c6-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="277c6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="277c6-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="277c6-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="277c6-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="277c6-123"><dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="277c6-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="277c6-124">Der Anbieter hat an einen Client mit einem Standard-DHCP-Antwortpaket geantwortet, das einen Pfad zum Netzwerkstart Programm enthält.</span><span class="sxs-lookup"><span data-stu-id="277c6-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="277c6-125">Die Rückgabe dieser Aktion bedeutet, dass der Anbieter die Client Anforderung erfolgreich abgeschlossen hat, indem er die [**pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion mindestens einmal aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="277c6-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="277c6-126"><dt>**PXE \_ BA \_ Benutzer**</dt> definiert <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="277c6-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="277c6-127">Der Anbieter hat eine benutzerdefinierte Antwort an einen Client geantwortet, die nicht den DHCP-Spezifikationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="277c6-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="277c6-128">Die Rückgabe dieser Aktion bedeutet, dass der Anbieter die Client Anforderung erfolgreich abgeschlossen hat, indem er die [**pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion mindestens einmal aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="277c6-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="277c6-129"><dt>**PXE \_ BA \_ Ignore**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="277c6-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="277c6-130">Der Anbieter möchte die Client Anforderung nicht bedienen, und die Anforderung sollte nicht an den nächsten Anbieter weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="277c6-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="277c6-131">Alle Ressourcen, die der Client Anforderung zugeordnet sind, werden freigegeben, und die Client Anforderung wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="277c6-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="277c6-132">Anbieter können diesen Wert auch verwenden, wenn Sie den Client erkennen, aber die Anforderung falsch formatiert war.</span><span class="sxs-lookup"><span data-stu-id="277c6-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="277c6-133"><dt>**PXE \_ BA \_ abgelehnt**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="277c6-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="277c6-134">Der Anbieter möchte die Client Anforderung nicht bedienen.</span><span class="sxs-lookup"><span data-stu-id="277c6-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="277c6-135">Das System übergibt die Anforderung an den nächsten Anbieter in der Liste der registrierten Anbieter.</span><span class="sxs-lookup"><span data-stu-id="277c6-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="277c6-136">Wenn dies der letzte Anbieter in der Liste ist, werden alle der Client Anforderung zugeordneten Ressourcen freigegeben, und die Client Anforderung wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="277c6-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="277c6-137">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277c6-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277c6-138">Der Kontextwert, der an die [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="277c6-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277c6-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="277c6-139">Return value</span></span>

<span data-ttu-id="277c6-140">Wenn der Anbieter die Client Anforderung erfolgreich verarbeitet hat, sollte der Rückruf **Fehler \_** erfolgreich zurückgeben, und die **PXE- \_ Start \_ Aktion** , auf die der *pAction* -Parameter verweist, enthält die entsprechende Start Aktion für diese Anforderung.</span><span class="sxs-lookup"><span data-stu-id="277c6-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="277c6-141">Wenn der Anbieter die Client Anforderung asynchron verarbeitet, sollte der Rückruf Fehler-e/a **\_ \_ Ausstehend** zurückgeben und die [**pxeasyncrecvdone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) -Funktion aufzurufen, wenn die Client Anforderung verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="277c6-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="277c6-142">Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden, und das System wird so fortgesetzt, als ob die von **PXE \_ BA \_ Abgelehnte** Start Aktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="277c6-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="277c6-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="277c6-143">Remarks</span></span>

<span data-ttu-id="277c6-144">Der Typ von Paketen, die von einem Anbieter erkannt werden, kann mit der [**pxeprovidersetattribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) -Funktion geändert werden.</span><span class="sxs-lookup"><span data-stu-id="277c6-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="277c6-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="277c6-145">Requirements</span></span>



| <span data-ttu-id="277c6-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="277c6-146">Requirement</span></span> | <span data-ttu-id="277c6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="277c6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="277c6-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="277c6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="277c6-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="277c6-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="277c6-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="277c6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="277c6-151">Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="277c6-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="277c6-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="277c6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277c6-153">Server Funktionen der Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="277c6-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="277c6-154">**Pxeregistercallback**</span><span class="sxs-lookup"><span data-stu-id="277c6-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="277c6-155">**Pxesendreply**</span><span class="sxs-lookup"><span data-stu-id="277c6-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="277c6-156">**Pxeproviderationtattribute**</span><span class="sxs-lookup"><span data-stu-id="277c6-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





