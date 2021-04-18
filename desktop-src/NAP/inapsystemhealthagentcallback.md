---
title: Inapsystemhealthagentcallback-Schnittstelle (napsystemhealthagent. h)
description: Werden vom System deklariert und vom SHA-Writer implementiert, damit der NAPAgent mit dem SHA kommunizieren kann.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- Inapsystemhealthagentcallback-Schnittstelle NAP
- Inapsystemhealthagentcallback-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341017"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="a9ed6-105">Inapsystemhealthagentcallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a9ed6-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="a9ed6-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a9ed6-107">Die **inapsystemhealthagentcallback** -Schnittstelle stellt Rückruf Methoden bereit, die vom System deklariert und vom SHA-Writer implementiert werden, damit der NAPAgent mit dem SHA kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="a9ed6-108">Member</span><span class="sxs-lookup"><span data-stu-id="a9ed6-108">Members</span></span>

<span data-ttu-id="a9ed6-109">Die **inapsystemhealthagentcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9ed6-110">**Inapsystemhealthagentcallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a9ed6-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="a9ed6-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a9ed6-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9ed6-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a9ed6-112">Methods</span></span>

<span data-ttu-id="a9ed6-113">Die **inapsystemhealthagentcallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="a9ed6-114">Methode</span><span class="sxs-lookup"><span data-stu-id="a9ed6-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="a9ed6-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9ed6-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9ed6-116">**Inapsystemhealthagentcallback:: comparesohrequests**</span><span class="sxs-lookup"><span data-stu-id="a9ed6-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="a9ed6-117">Wird vom SHA zum Vergleichen der SoHs verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="a9ed6-118">**Inapsystemhealthagentcallback:: getfixupinfo**</span><span class="sxs-lookup"><span data-stu-id="a9ed6-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="a9ed6-119">Wird von NAPAgent aufgerufen, um den Zustand des SHA zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="a9ed6-120">**Inapsystemhealthagentcallback:: getsohrequest**</span><span class="sxs-lookup"><span data-stu-id="a9ed6-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="a9ed6-121">Wird von NAPAgent aufgerufen, um die SoH-Anforderung des SHA abzufragen.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="a9ed6-122">**Inapsystemhealthagentcallback:: notieyorphanedsohrequest**</span><span class="sxs-lookup"><span data-stu-id="a9ed6-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="a9ed6-123">Wird aufgerufen, wenn eine SoH-Anforderung vom SHA abgefragt wurde, die Antwort jedoch nie zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="a9ed6-124">**Inapsystemhealthagentcallback:: notifysystemsolationstatechange**</span><span class="sxs-lookup"><span data-stu-id="a9ed6-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="a9ed6-125">Wird von NAPAgent aufgerufen, um anzugeben, dass sich der System Isolations Status oder die Endzeit der Bewährungszeit geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="a9ed6-126">**Inapsystemhealthagentcallback::P rocesssohresponse**</span><span class="sxs-lookup"><span data-stu-id="a9ed6-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="a9ed6-127">Wird aufgerufen, wenn NAPAgent eine SoH-Antwort empfängt, die für diesen Integritäts-Agent bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="a9ed6-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="a9ed6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9ed6-128">Requirements</span></span>



| <span data-ttu-id="a9ed6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9ed6-129">Requirement</span></span> | <span data-ttu-id="a9ed6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a9ed6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ed6-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9ed6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ed6-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9ed6-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9ed6-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9ed6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ed6-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9ed6-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9ed6-135">Header</span><span class="sxs-lookup"><span data-stu-id="a9ed6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9ed6-136"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ed6-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9ed6-137">IDL</span><span class="sxs-lookup"><span data-stu-id="a9ed6-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9ed6-138"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9ed6-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ed6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ed6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ed6-140">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a9ed6-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a9ed6-141">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="a9ed6-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

