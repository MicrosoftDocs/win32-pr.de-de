---
title: Inapsystemhealthagentbinding-Schnittstelle (napsystemhealthagent. h)
description: Die SHAs, die für die Kommunikation mit dem NAPAgent verwendet werden. | Inapsystemhealthagentbinding-Schnittstelle (napsystemhealthagent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- Inapsystemhealthagentbinding-Schnittstelle NAP
- Inapsystemhealthagentbinding-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363947"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="1002b-106">Inapsystemhealthagentbinding-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1002b-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="1002b-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1002b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1002b-108">**Inapsystemhealthagentbinding** stellt Methoden bereit, die von den SHAs für die Kommunikation mit dem NAPAgent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1002b-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="1002b-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1002b-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="1002b-110">Member</span><span class="sxs-lookup"><span data-stu-id="1002b-110">Members</span></span>

<span data-ttu-id="1002b-111">Die **inapsystemhealthagentbinding** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1002b-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1002b-112">**Inapsystemhealthagentbinding** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1002b-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="1002b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="1002b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1002b-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="1002b-114">Methods</span></span>

<span data-ttu-id="1002b-115">Die **inapsystemhealthagentbinding** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1002b-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="1002b-116">Methode</span><span class="sxs-lookup"><span data-stu-id="1002b-116">Method</span></span>                                                                                                                     | <span data-ttu-id="1002b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1002b-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1002b-118">**Inapsystemhealthagentbinding:: FLUSHCACHE**</span><span class="sxs-lookup"><span data-stu-id="1002b-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="1002b-119">Wird von einem SHA aufgerufen, um den SoH-Cache zu leeren.</span><span class="sxs-lookup"><span data-stu-id="1002b-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="1002b-120">**Inapsystemhealthagentbinding:: getsystemsolationinfo**</span><span class="sxs-lookup"><span data-stu-id="1002b-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="1002b-121">Wird von SHAs aufgerufen, um den systemisolations Status zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1002b-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="1002b-122">**Inapsystemhealthagentbinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1002b-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="1002b-123">Initialisiert das SHA und bindet das SHA an den NAPAgent-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1002b-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="1002b-124">**Inapsystemhealthagentbinding:: notifysohchange**</span><span class="sxs-lookup"><span data-stu-id="1002b-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="1002b-125">Wird von SHAs aufgerufen, wenn sich Ihr SoH ändert.</span><span class="sxs-lookup"><span data-stu-id="1002b-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="1002b-126">**Inapsystemhealthagentbinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="1002b-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="1002b-127">Wird von SHAs aufgerufen, damit der NAPAgent alle Verweise auf SHA-com-Zeiger freigibt.</span><span class="sxs-lookup"><span data-stu-id="1002b-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1002b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1002b-128">Remarks</span></span>

<span data-ttu-id="1002b-129">Alle APIs in dieser Schnittstelle geben **RPC \_ E \_ getrennt** zurück, wenn der NAPAgent angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="1002b-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="1002b-130">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="1002b-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="1002b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1002b-131">Requirements</span></span>



| <span data-ttu-id="1002b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1002b-132">Requirement</span></span> | <span data-ttu-id="1002b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1002b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1002b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1002b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1002b-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1002b-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1002b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1002b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1002b-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1002b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1002b-138">Header</span><span class="sxs-lookup"><span data-stu-id="1002b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1002b-139"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="1002b-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="1002b-140">IDL</span><span class="sxs-lookup"><span data-stu-id="1002b-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1002b-141"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1002b-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="1002b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1002b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1002b-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1002b-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1002b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1002b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1002b-145">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1002b-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1002b-146">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="1002b-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

