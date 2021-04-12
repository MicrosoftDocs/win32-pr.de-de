---
title: Inapsystemhealthagentrequest-Schnittstelle (napsystemhealthagent. h)
description: SHAs verwenden Sie, um die Verarbeitung mit dem NAP-System zu kommunizieren und zu koordinieren.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- Inapsystemhealthagentrequest-Schnittstelle NAP
- Inapsystemhealthagentrequest-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517705"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="f8541-105">Inapsystemhealthagentrequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f8541-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="f8541-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8541-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f8541-107">Die **inapsystemhealthagentrequest** -Schnittstelle stellt Methoden bereit, die von SHAs zum kommunizieren und koordinieren der Verarbeitung mit dem NAP-System verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8541-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="f8541-108">Member</span><span class="sxs-lookup"><span data-stu-id="f8541-108">Members</span></span>

<span data-ttu-id="f8541-109">Die **inapsystemhealthagentrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f8541-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f8541-110">**Inapsystemhealthagentrequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f8541-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="f8541-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f8541-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f8541-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f8541-112">Methods</span></span>

<span data-ttu-id="f8541-113">Die **inapsystemhealthagentrequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f8541-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="f8541-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f8541-114">Method</span></span>                                                                                                                     | <span data-ttu-id="f8541-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8541-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8541-116">**Inapsystemhealthagentrequest:: getcachesohflag**</span><span class="sxs-lookup"><span data-stu-id="f8541-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="f8541-117">Wird nur von NAPAgent verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8541-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="f8541-118">**Inapsystemhealthagentrequest:: getcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="f8541-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="f8541-119">Wird von Systemintegritäts-Agents verwendet, um SoHs und [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="f8541-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="f8541-120">**Inapsystemhealthagentrequest:: getsohrequest**</span><span class="sxs-lookup"><span data-stu-id="f8541-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="f8541-121">Wird von SHAs verwendet, um SoHs zu erhalten, die zuvor vom NAPAgent zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="f8541-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="f8541-122">**Inapsystemhealthagentrequest:: getsohresponse**</span><span class="sxs-lookup"><span data-stu-id="f8541-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="f8541-123">Wird vom Integritäts-Agent zum Abrufen der [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8541-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="f8541-124">**Inapsystemhealthagentrequest:: getstringcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="f8541-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="f8541-125">Wird von Systemintegritäts-Agents zum Protokollieren der Korrelations-ID verwendet</span><span class="sxs-lookup"><span data-stu-id="f8541-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="f8541-126">**Inapsystemhealthagentrequest:: setsohrequest**</span><span class="sxs-lookup"><span data-stu-id="f8541-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="f8541-127">Wird von Health-Agents zum Schreiben der SoH-Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8541-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="f8541-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8541-128">Requirements</span></span>



| <span data-ttu-id="f8541-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8541-129">Requirement</span></span> | <span data-ttu-id="f8541-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f8541-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8541-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8541-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f8541-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8541-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8541-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8541-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f8541-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8541-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8541-135">Header</span><span class="sxs-lookup"><span data-stu-id="f8541-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8541-136"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8541-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8541-137">IDL</span><span class="sxs-lookup"><span data-stu-id="f8541-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8541-138"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8541-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="f8541-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f8541-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8541-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8541-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="f8541-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8541-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8541-142">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f8541-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f8541-143">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="f8541-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

