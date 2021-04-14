---
title: INapSystemHealthAgentBinding2-Schnittstelle (napsystemhealthagent. h)
description: Die SHAs, die für die Kommunikation mit dem NAPAgent verwendet werden. | INapSystemHealthAgentBinding2-Schnittstelle (napsystemhealthagent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2-Schnittstelle NAP
- INapSystemHealthAgentBinding2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352798"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="42957-106">INapSystemHealthAgentBinding2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="42957-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="42957-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42957-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="42957-108">**INapSystemHealthAgentBinding2** stellt Methoden bereit, die von den SHAs für die Kommunikation mit dem NAPAgent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42957-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="42957-109">Diese Schnittstelle erbt alle Methoden von [**inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md) und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42957-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="42957-110">Member</span><span class="sxs-lookup"><span data-stu-id="42957-110">Members</span></span>

<span data-ttu-id="42957-111">Die **INapSystemHealthAgentBinding2** -Schnittstelle erbt von [**inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md).</span><span class="sxs-lookup"><span data-stu-id="42957-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="42957-112">**INapSystemHealthAgentBinding2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="42957-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="42957-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="42957-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="42957-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="42957-114">Methods</span></span>

<span data-ttu-id="42957-115">Die **INapSystemHealthAgentBinding2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="42957-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="42957-116">Methode</span><span class="sxs-lookup"><span data-stu-id="42957-116">Method</span></span>                                                                                                                    | <span data-ttu-id="42957-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42957-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42957-118">**INapSystemHealthAgentBinding2:: getsystemisolationinfoex**</span><span class="sxs-lookup"><span data-stu-id="42957-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="42957-119">Wird von SHAs aufgerufen, um den systemisolations Zustand und den erweiterten Isolations Status zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="42957-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42957-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42957-120">Remarks</span></span>

<span data-ttu-id="42957-121">Alle APIs in dieser Schnittstelle geben **RPC \_ E \_ getrennt** zurück, wenn der NAPAgent angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="42957-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="42957-122">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="42957-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="42957-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42957-123">Requirements</span></span>



| <span data-ttu-id="42957-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42957-124">Requirement</span></span> | <span data-ttu-id="42957-125">Wert</span><span class="sxs-lookup"><span data-stu-id="42957-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42957-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42957-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42957-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42957-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="42957-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42957-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42957-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42957-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="42957-130">Header</span><span class="sxs-lookup"><span data-stu-id="42957-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="42957-131"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="42957-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="42957-132">IDL</span><span class="sxs-lookup"><span data-stu-id="42957-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42957-133"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42957-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="42957-134">DLL</span><span class="sxs-lookup"><span data-stu-id="42957-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42957-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42957-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="42957-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42957-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42957-137">**Inapsystemhealthagentbinding**</span><span class="sxs-lookup"><span data-stu-id="42957-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="42957-138">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="42957-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="42957-139">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="42957-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





