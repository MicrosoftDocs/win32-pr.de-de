---
title: Inapsystemhealthvalidator Validate-Methode (napsystemhealthvalidator. h)
description: Das NAP-System zum Überprüfen der sohrequest, die von einem Client empfangen wurde.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validate-Methode für NAP
- Validate-Methode, NAP, inapsystemhealthvalidator-Schnittstelle
- Inapsystemhealthvalidator-Schnittstelle NAP, Validate-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337920"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="cddbe-106">Inapsystemhealthvalidator:: Validate-Methode</span><span class="sxs-lookup"><span data-stu-id="cddbe-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="cddbe-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cddbe-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cddbe-108">Die **inapsystemhealthvalidator:: Validate** -Methode wird vom SHV-Entwickler definiert und vom NAP-System aufgerufen, um die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) zu validieren, die von einem Client empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="cddbe-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddbe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cddbe-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="cddbe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cddbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cddbe-111">*Anforderung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cddbe-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cddbe-112">Ein com-Zeiger auf ein [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md) -Objekt, das das Validierungs Anforderungs Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cddbe-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="cddbe-113">*hinttimeoutinmsec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cddbe-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cddbe-114">Die Dauer des Kommunikations Timeout Zeitraums in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="cddbe-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="cddbe-115">Der System Integritäts Prüfungs Punkt (System Health Validator, SHV) sollte innerhalb dieser Zeitspanne Antworten. Andernfalls wird die Antwort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cddbe-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="cddbe-116">Das Standard Timeout für alle SHVs beträgt 2000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="cddbe-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="cddbe-117">Wenn Sie einen anderen Wert als den Standardwert verwenden, wird das Timeout für alle registrierten SHVs geändert.</span><span class="sxs-lookup"><span data-stu-id="cddbe-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="cddbe-118">*Rückruf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cddbe-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cddbe-119">Ein Zeiger auf das Rückruf Objekt [**inapservercallback**](inapservercallback.md).</span><span class="sxs-lookup"><span data-stu-id="cddbe-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="cddbe-120">Dieser Rückruf Zeiger wird von den SHVs verwendet, wenn er aus dem Aufrufen von **inapsystemhealthvalidator:: Validate** **E \_** aussteht.</span><span class="sxs-lookup"><span data-stu-id="cddbe-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="cddbe-121">Diese wird für die asynchrone Validierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cddbe-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="cddbe-122">Es wird erwartet, dass die SHVs innerhalb der *hinttimeoutinmsec* -Zeit reagieren, oder andernfalls wird die Antwort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cddbe-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cddbe-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cddbe-123">Return value</span></span>

<span data-ttu-id="cddbe-124">Wenn ein anderer Fehlercode zurückgegeben wird, geht das System davon aus, dass der Server Component-Fehler aufgetreten ist, und die entsprechende Zuordnung erfolgt, um erfolgreich bzw. fehlerhaft zu sein.</span><span class="sxs-lookup"><span data-stu-id="cddbe-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="cddbe-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cddbe-125">Return code</span></span>                                                                                                | <span data-ttu-id="cddbe-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cddbe-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cddbe-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="cddbe-128">Gibt an, dass das Validierungs Steuerelement für das Objekt "Request" eine sohresponse festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="cddbe-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="cddbe-129"><dt>**E \_ Ausstehend**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="cddbe-130">Gibt an, dass OnComplete () in einem separaten Thread aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cddbe-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="cddbe-131"><dt>**RPC \_ S- \_ Server nicht \_ verfügbar**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="cddbe-132">Gibt an, dass der SHV-Prozess (System Health Validator) beendet wurde, ohne dass der napserver einen Verweis darauf freigibt.</span><span class="sxs-lookup"><span data-stu-id="cddbe-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="cddbe-133">Der napserver versucht erneut, einen neuen Verweis auf den SHV zu erstellen und führt den Validate-Rückruf einmal erneut aus.</span><span class="sxs-lookup"><span data-stu-id="cddbe-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="cddbe-134">Wenn bei der Erstellung des Objekts oder der erneut ausgeführten Überprüfung ein Fehler auftritt, wird der SHV aus der Liste der geladenen SHVs entfernt.</span><span class="sxs-lookup"><span data-stu-id="cddbe-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="cddbe-135">Dieser SHV kann nun nur erneut geladen werden, indem die Registrierung und die erneute Registrierung des SHV erneut aufgehoben werden, oder wenn der napserver neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cddbe-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cddbe-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cddbe-136">Remarks</span></span>

<span data-ttu-id="cddbe-137">Um die Erkennung von Eindring Versuchen zu unterstützen, werden SHVs aufgefordert, den Client Computer zu validieren, unabhängig davon, ob der Client einen für den SHV vorgesehenen [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="cddbe-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="cddbe-138">Der SHV muss folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="cddbe-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="cddbe-139">Rufen Sie den [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) aus der *Anforderung* ab, indem Sie [**Request aufrufen. Getsohrequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="cddbe-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="cddbe-140">Wenn das [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket NULL ist:</span><span class="sxs-lookup"><span data-stu-id="cddbe-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="cddbe-141">Wenn der SHV ein Angriffs Erkennungssystem ist, füllen Sie ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket mit dem entsprechenden [**NAP-Fehlercode**](nap-error-constants.md) aus, um zu ermitteln, warum der Client Computer schädlich ist.</span><span class="sxs-lookup"><span data-stu-id="cddbe-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="cddbe-142">Alle anderen SHVs sollten ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket mit dem Fehlercode " [**NAP \_ E \_ Missing \_ SoH**](nap-error-constants.md)" auffüllen.</span><span class="sxs-lookup"><span data-stu-id="cddbe-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="cddbe-143">Wenn ' *napsystemgenerated* ' vom Anforderungs Aufrufwert ' **true** ' ist [**. Getsohrequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), der SHV sollte ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket mit den folgenden 3 TLVS erwarten: [**sohattributetypesystemhealthid**](sohattributetype-enum.md), **sohattributetypefailurecategory**, **sohattributetypeerrorcodes**.</span><span class="sxs-lookup"><span data-stu-id="cddbe-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="cddbe-144">Dieser **sohrequest** wird vom NAPAgent im Auftrag des Systemintegritäts-Agents (SHA) generiert, weil beim Abrufen eines Anforderungs Pakets aus dem SHA ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cddbe-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="cddbe-145">Überprüfen Sie das [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.</span><span class="sxs-lookup"><span data-stu-id="cddbe-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="cddbe-146">Wenn die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) falsch formatiert ist, erstellen Sie ein **sohresponse** -Paket mit dem Fehlercode [**NAP \_ E \_ ungültiges \_ Paket**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cddbe-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="cddbe-147">Wenn der SHV nur zwischengespeicherte Informationen für die Überprüfung des [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets verwendet (d. h. keine e/a-Vorgänge durchgeführt werden), kann er **sohresponse** erstellen, ihn für das Objekt in der *Anforderung* festlegen und **S \_ OK** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cddbe-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="cddbe-148">Wenn der SHV e/a-Vorgänge ausführt, um mit den Back-End-Servern zum Überprüfen der Integrität des Clients zu kommunizieren, muss er die E/a in die Warteschlange stellen und diese Funktion mit **E \_ Pending** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cddbe-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="cddbe-149">In diesem Fall muss der SHV Callback aufrufen [**. OnComplete ()**](inapservercallback-oncomplete-method.md) in einem separaten Thread innerhalb des Timeout Zeitraums *hinttimeoutinmsec*.</span><span class="sxs-lookup"><span data-stu-id="cddbe-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="cddbe-150">Andernfalls wird die Antwort des SHV gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cddbe-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="cddbe-151">Geben Sie außer den oben aufgeführten Fehlern keinen anderen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="cddbe-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="cddbe-152">Wenn vom SHV ein anderer Fehlercode zurückgegeben wird (z. b.</span><span class="sxs-lookup"><span data-stu-id="cddbe-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="cddbe-153">Systemfehler), wird das Paket verworfen.</span><span class="sxs-lookup"><span data-stu-id="cddbe-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="cddbe-154">Ein SHV muss entweder einen **sohattributetypecomplianceresultcodes** oder **sohattributetypefailurecategory** TLV in seinem [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cddbe-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="cddbe-155">[**sohattributetypecomplianceresultcodes TLV**](sohattributetype-enum.md): Wenn die Integrität des Clients von SHV überprüft werden konnte (d. h. fehlerfrei oder fehlerhaft), wird dieses TLV zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cddbe-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="cddbe-156">[**sohattributetypefailurecategory TLV**](sohattributetype-enum.md): Wenn auf dem Client oder Server ein Komponenten-oder Kommunikationsfehler aufgetreten ist, muss dies von diesem TLV angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cddbe-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="cddbe-157">Dieses TLV wird in Abhängigkeit von der Konfiguration des SHV weiterhin fehlerfrei oder fehlerfrei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cddbe-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="cddbe-158">Weitere Informationen finden Sie unter der [**inapservermanagement**](inapservermanagement.md) -Schnittstelle und der [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cddbe-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="cddbe-159">Der SHV darf keine Verweise auf die *Anforderung* oder den *Rückruf* enthalten, wenn der asynchrone-Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cddbe-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="cddbe-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cddbe-160">Requirements</span></span>



| <span data-ttu-id="cddbe-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cddbe-161">Requirement</span></span> | <span data-ttu-id="cddbe-162">Wert</span><span class="sxs-lookup"><span data-stu-id="cddbe-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cddbe-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cddbe-163">Minimum supported client</span></span><br/> | <span data-ttu-id="cddbe-164">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cddbe-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="cddbe-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cddbe-165">Minimum supported server</span></span><br/> | <span data-ttu-id="cddbe-166">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cddbe-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cddbe-167">Header</span><span class="sxs-lookup"><span data-stu-id="cddbe-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="cddbe-168"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="cddbe-169">IDL</span><span class="sxs-lookup"><span data-stu-id="cddbe-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cddbe-170"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cddbe-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cddbe-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cddbe-172">**Inapsystemhealthvalidator**</span><span class="sxs-lookup"><span data-stu-id="cddbe-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





