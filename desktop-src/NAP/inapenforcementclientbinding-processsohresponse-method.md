---
title: Inapenforcementclientbinding processsohresponse-Methode (napforcementclient. h)
description: Wird von Erzwingungs Clients verwendet, um eine sohresponse zu verarbeiten, wenn Sie ein sohresponse-datenblob von dem Erzwingungs Server erhalten.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Processsohresponse-Methode NAP
- Processsohresponse-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, processsohresponse-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519175"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="144f2-106">Inapenforcementclientbinding::P rocesssohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="144f2-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="144f2-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="144f2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="144f2-108">Die **inapenforcementclientbinding::P rocesssohresponse** -Methode wird von Erzwingungs Clients verwendet, um eine sohresponse zu verarbeiten, wenn Sie ein sohresponse-datenblob von dem Erzwingungs Server erhalten.</span><span class="sxs-lookup"><span data-stu-id="144f2-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="144f2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="144f2-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="144f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="144f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="144f2-111">*Verbindung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="144f2-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144f2-112">Ein com-Zeiger auf die [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle der Client Verbindung.</span><span class="sxs-lookup"><span data-stu-id="144f2-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="144f2-113">Der NAPAgent enthält keine Verweise auf das Objekt, das dieser Schnittstelle zugeordnet ist, nachdem dieser Methoden Aufrufvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="144f2-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="144f2-114">Sie müssen eine zuvor festgelegte Verbindung für die Verarbeitung von sohresponse-datenblobvorgängen verwenden.</span><span class="sxs-lookup"><span data-stu-id="144f2-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="144f2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="144f2-115">Return value</span></span>

<span data-ttu-id="144f2-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="144f2-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="144f2-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="144f2-117">Return code</span></span>                                                                                             | <span data-ttu-id="144f2-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="144f2-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="144f2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="144f2-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="144f2-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="144f2-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="144f2-122">Auf dem Erzwingungs Client wurden zuvor keine Verbindungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="144f2-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="144f2-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="144f2-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="144f2-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="144f2-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="144f2-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="144f2-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="144f2-127"><dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="144f2-128">Wenn dieser Wert zurückgegeben wird, muss der Erzwingungs Client das Paket löschen, wenn der NAPAgent ein ungültiges NAP-Paket zurückgibt \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="144f2-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="144f2-129">In diesem Fall muss der Enforcer davon ausgehen, dass der Server, mit dem er kommuniziert, nicht NAP-fähig ist, und die Verbindung aus der aktiven Liste entfernen (d. h., der NAPAgent wird über einen Verbindungsstatus benachrichtigt).</span><span class="sxs-lookup"><span data-stu-id="144f2-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="144f2-130"><dt>**nicht \_ \_ übereinstimmende NAP- \_ ID**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="144f2-131">Wenn dieser Wert zurückgegeben wird, weist dies darauf hin, dass die Korrelations-ID im SoH-Response Paket nicht mit der ausstehenden SoH-Antwort identisch war.</span><span class="sxs-lookup"><span data-stu-id="144f2-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="144f2-132">In diesem Fall sollte der Enforcer das Paket löschen und auf ein anderes neueres SoH-Response Paket warten.</span><span class="sxs-lookup"><span data-stu-id="144f2-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="144f2-133">Dies kann durch eine Antwort auf eine ältere Anforderungs Nachricht verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="144f2-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="144f2-134"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="144f2-135">Der Enforcer wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="144f2-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="144f2-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="144f2-136">Remarks</span></span>

<span data-ttu-id="144f2-137">Der NAPAgent fragt den SoH-Response Data BLOB aus dem Verbindungs Objekt ab, verarbeitet ihn und legt die resultierende Entscheidung fest (z. b.</span><span class="sxs-lookup"><span data-stu-id="144f2-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="144f2-138">vollständiger/eingeschränkter Zugriff/usw.) für das Verbindungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="144f2-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="144f2-139">Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="144f2-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="144f2-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="144f2-140">Requirements</span></span>



| <span data-ttu-id="144f2-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="144f2-141">Requirement</span></span> | <span data-ttu-id="144f2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="144f2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="144f2-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="144f2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="144f2-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="144f2-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="144f2-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="144f2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="144f2-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="144f2-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="144f2-147">Header</span><span class="sxs-lookup"><span data-stu-id="144f2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="144f2-148"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="144f2-149">IDL</span><span class="sxs-lookup"><span data-stu-id="144f2-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="144f2-150"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="144f2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="144f2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="144f2-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="144f2-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="144f2-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="144f2-153">See also</span></span>

<dl> <span data-ttu-id="144f2-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="144f2-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="144f2-155">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="144f2-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="144f2-156">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="144f2-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





