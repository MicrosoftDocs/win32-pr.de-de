---
title: Inapsystemhealthagentcallback getsohrequest-Methode (napsystemhealthagent. h)
description: Wird von NAPAgent aufgerufen, um die SoH-Anforderung des Systemintegritäts-Agents abzufragen.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392001"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="c5d3a-106">Inapsystemhealthagentcallback:: getsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="c5d3a-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="c5d3a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c5d3a-108">Die **inapsystemhealthagentcallback:: getsohrequest** -Methode wird von NAPAgent aufgerufen, um die SoH-Anforderung des Systemintegritäts-Agents abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d3a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d3a-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="c5d3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5d3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d3a-111">*Anforderung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5d3a-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d3a-112">Ein com-Zeiger auf ein [**inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md) -Objekt, das das Anforderungs Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d3a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5d3a-113">Return value</span></span>



| <span data-ttu-id="c5d3a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c5d3a-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="c5d3a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5d3a-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5d3a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5d3a-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="c5d3a-117">Gibt die erfolgreiche Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="c5d3a-118"><dt>**HRESULT \_ von \_ Win32 (RPC \_ S- \_ Server nicht \_ verfügbar)**</dt></span><span class="sxs-lookup"><span data-stu-id="c5d3a-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="c5d3a-119">Wenn dieser Code von ihrer Implementierung zurückgegeben wird, entfernt der NAPAgent den SHA-Eintrag aus der gebundenen SHA-Liste und leert seinen Cache Eintrag.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="c5d3a-120">Wenn ein beliebiger Rückgabewert (mit Ausnahme **von HRESULT \_ von \_ Win32 (RPC \_ S-Server nicht \_ \_ verfügbar)**) von ihrer Implementierung zurückgegeben wird, erstellt das NAP-System eine [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und gibt Sie mit den folgenden Attributtypen und Werten an den entsprechenden SHV zurück:</span><span class="sxs-lookup"><span data-stu-id="c5d3a-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="c5d3a-121">[**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="c5d3a-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="c5d3a-122">[**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcomponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="c5d3a-123">[**sohattributetypeerrorcodes**](sohattributetype-enum.md) = <Fehlercode></span><span class="sxs-lookup"><span data-stu-id="c5d3a-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="c5d3a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5d3a-124">Remarks</span></span>

<span data-ttu-id="c5d3a-125">Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="c5d3a-126">Diese Methode muss die Anforderung verarbeiten und sofort zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="c5d3a-127">Das Verzögern der Rückgabe dieser Methode wirkt sich negativ auf die Systemleistung und die Reaktionsfähigkeit aus und kann dazu führen, dass für andere Teile des Betriebssystems ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="c5d3a-128">Die Überwachung des Integritäts Zustands sollte nicht als Teil dieses Aufrufes erfolgen, insbesondere wenn es sich um eine rechenintensive Berechnung handelt und einige Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="c5d3a-129">Die Integritäts Zustandsüberwachung und die SoH-Berechnung sollten in einem separaten Thread oder Dienst durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="c5d3a-130">Die einzige Funktion dieser Methode sollte sein, das SoH von SHA festzulegen und zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="c5d3a-131">Wenn es lange dauern wird, bis das SHA ein SoH generiert, sollte das zwischengespeicherte SoH an den NAPAgent zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="c5d3a-132">Wenn kein zwischengespeichertes SoH vorhanden ist, sollte das SHA sofort ein SoH mit den folgenden Attributtypen und Werten zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="c5d3a-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="c5d3a-133">[**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="c5d3a-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="c5d3a-134">[**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="c5d3a-135">[**sohattributetypeerrorcodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ kein \_ zwischengespeichertes \_ SoH**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="c5d3a-136">Wenn das SoH generiert wurde, muss das SHA [**inapsystemhealthagentbinding:: notifysohchange**](inapsystemhealthagentbinding-notifysohchange-method.md) aufgerufen werden, um den NAPAgent über die System Integritäts Änderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="c5d3a-137">Der NAPAgent ruft diese Methode auf, um den sohrequest des Systemintegritäts-Agents abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="c5d3a-138">Der SHA kann das bestandene [**inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md) -Objekt nach Parametern Abfragen, die es benötigt, um den sohrequest zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="c5d3a-139">Der SHA muss die berechnete sohrequest für das Anforderungs Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="c5d3a-140">Der SHA darf keine Verweise auf das Anforderungs Objekt enthalten, nachdem dieser-Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="c5d3a-141">Wenn diese Methode aufgerufen wird und ein SoH im Cache von NAPAgent vorhanden ist, wird Sie für das Anforderungs Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="c5d3a-142">Der SHA kann ihn mithilfe von **getsohrequest** Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="c5d3a-143">Wenn das SHA kein neues SoH festgelegt, wird das zwischengespeicherte verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5d3a-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="c5d3a-144">Für ungebundene SHAs, die beim System registriert sind, erstellt das NAP-System eine sohrequest und sendet Sie an den entsprechenden SHV mit den folgenden Attributtypen und Werten:</span><span class="sxs-lookup"><span data-stu-id="c5d3a-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="c5d3a-145">[**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="c5d3a-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="c5d3a-146">[**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcomponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="c5d3a-147">[**sohattributetypeerrorcodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ nicht \_ Initialisiert**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d3a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5d3a-148">Requirements</span></span>



| <span data-ttu-id="c5d3a-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5d3a-149">Requirement</span></span> | <span data-ttu-id="c5d3a-150">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d3a-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d3a-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d3a-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5d3a-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5d3a-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5d3a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d3a-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5d3a-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5d3a-155">Header</span><span class="sxs-lookup"><span data-stu-id="c5d3a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d3a-156"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d3a-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5d3a-157">IDL</span><span class="sxs-lookup"><span data-stu-id="c5d3a-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5d3a-158"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5d3a-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d3a-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5d3a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d3a-160">**Inapsystemhealthagentcallback**</span><span class="sxs-lookup"><span data-stu-id="c5d3a-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





