---
title: Inapsystemhealthagentcallback notifis-Benachrichtigungsmethode (napsystemhealthagent. h)
description: Wird aufgerufen, wenn ein sohrequest vom SHA abgefragt wurde, die Antwort jedoch nie zurückgegeben wurde.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Notisyorphanedsohrequest-Methode NAP
- Notisyorphanedsohrequest-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, notitelyorphanedsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392178"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="3e3fa-106">Inapsystemhealthagentcallback:: notieyorphanedsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="3e3fa-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="3e3fa-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3e3fa-108">Die **inapsystemhealthagentcallback:: notifyorphanedsohrequest** -Methode wird aufgerufen, wenn ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) vom SHA abgefragt wurde, die Antwort jedoch nie zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3fa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e3fa-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="3e3fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e3fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e3fa-111">*correlationId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e3fa-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3fa-112">Ein Zeiger auf die eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die den verwaisten [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e3fa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e3fa-113">Return value</span></span>

<span data-ttu-id="3e3fa-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3e3fa-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3e3fa-115">Return code</span></span>                                                                          | <span data-ttu-id="3e3fa-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e3fa-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="3e3fa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e3fa-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3e3fa-118">Gibt die erfolgreiche Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e3fa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e3fa-119">Remarks</span></span>

<span data-ttu-id="3e3fa-120">Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="3e3fa-121">Diese Methode kann vom System in den folgenden Fällen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="3e3fa-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="3e3fa-122">Ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) konnte nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="3e3fa-123">Ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) wurde über das Netzwerk gesendet, aber es wurde kein **sohresponse** zurückgegeben, d. h., es ist ein Timeout für den enforcern aufgetreten, oder auf der Serverseite ist kein entsprechender SHV vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="3e3fa-124">Die Verbindung wurde heruntergefahren, oder ein Enforcer wurde offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="3e3fa-125">Dies ist nur eine bestmögliche Benachrichtigung, daher dürfen sich SHAs nicht auf diese Informationen verlassen, um den Status zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="3e3fa-126">Es gibt mehrere Situationen, in denen ein SHA nicht benachrichtigt wird:</span><span class="sxs-lookup"><span data-stu-id="3e3fa-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="3e3fa-127">Wenn ein Enforcer falsch verhält, bedeutet dies, dass das SHA nicht benachrichtigt wird, wenn der Verbindungsstatus nicht erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="3e3fa-128">, Wenn ein-Enforcer abstürzt.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="3e3fa-129">In Fehlerzuständen, d. h., der NAPAgent verfügt nicht über genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="3e3fa-130">SHAs erhalten möglicherweise falsche Benachrichtigungen, wenn Sie zum ersten Mal eine Bindung an den NAPAgent herstellen, z. b. Wenn ein SoH-Austausch ausgeführt wird, wenn der SHA-gebunden ist, und dann ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="3e3fa-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3fa-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e3fa-131">Requirements</span></span>



| <span data-ttu-id="3e3fa-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e3fa-132">Requirement</span></span> | <span data-ttu-id="3e3fa-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3e3fa-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3fa-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e3fa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3e3fa-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e3fa-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3e3fa-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e3fa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3e3fa-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e3fa-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3e3fa-138">Header</span><span class="sxs-lookup"><span data-stu-id="3e3fa-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e3fa-139"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e3fa-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e3fa-140">IDL</span><span class="sxs-lookup"><span data-stu-id="3e3fa-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e3fa-141"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e3fa-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e3fa-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e3fa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3fa-143">**Inapsystemhealthagentcallback**</span><span class="sxs-lookup"><span data-stu-id="3e3fa-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





