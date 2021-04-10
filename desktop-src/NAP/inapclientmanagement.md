---
title: Inapclientmanagement-Schnittstelle (napmanagement. h)
description: Stellt Methoden für die NAP-Client Verwaltung bereit. | Inapclientmanagement-Schnittstelle (napmanagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- Inapclientmanagement-Schnittstelle NAP
- Inapclientmanagement Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961446"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="cfe0d-106">Inapclientmanagement-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cfe0d-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="cfe0d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cfe0d-108">Die **inapclientmanagement** -Schnittstelle bietet Methoden für die NAP-Client Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="cfe0d-109">[**INapClientManagement2**](inapclientmanagement2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="cfe0d-110">Member</span><span class="sxs-lookup"><span data-stu-id="cfe0d-110">Members</span></span>

<span data-ttu-id="cfe0d-111">Die **inapclientmanagement** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cfe0d-112">**Inapclientmanagement** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cfe0d-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="cfe0d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="cfe0d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cfe0d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="cfe0d-114">Methods</span></span>

<span data-ttu-id="cfe0d-115">Die **inapclientmanagement** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="cfe0d-116">Methode</span><span class="sxs-lookup"><span data-stu-id="cfe0d-116">Method</span></span>                                                                                                                | <span data-ttu-id="cfe0d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfe0d-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="cfe0d-118">**Inapclientmanagement:: getnapclientinfo**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="cfe0d-119">Ruft Informationen zu einem NAP-Client ab.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="cfe0d-120">**Inapclientmanagement:: getregisteredenforcementclients**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="cfe0d-121">Ruft Informationen zu den registrierten Erzwingungs Clients ab.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="cfe0d-122">**Inapclientmanagement:: getregisteredsystemhealthagents**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="cfe0d-123">Abrufen von Informationen zu einem registrierten SHA.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="cfe0d-124">**Inapclientmanagement:: getsystemisolationinfo**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="cfe0d-125">Ruft Informationen zum Isolations Status des NAP-Clients ab.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="cfe0d-126">**Inapclientmanagement:: registerenforcementclient**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="cfe0d-127">Registriert einen Erzwingungs Client beim NAP-System.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="cfe0d-128">**Inapclientmanagement:: registersystemhealthagent**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="cfe0d-129">Registriert einen SHA beim NAP-System.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="cfe0d-130">**Inapclientmanagement:: unregisterenforcementclient**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="cfe0d-131">Hebt die Registrierung eines Erzwingungs Clients beim NAP-System auf.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="cfe0d-132">**Inapclientmanagement:: unregistersystemhealthagent**</span><span class="sxs-lookup"><span data-stu-id="cfe0d-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="cfe0d-133">Hebt die Registrierung eines SHA beim NAP-System auf.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="cfe0d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfe0d-134">Requirements</span></span>



| <span data-ttu-id="cfe0d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfe0d-135">Requirement</span></span> | <span data-ttu-id="cfe0d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="cfe0d-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe0d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfe0d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe0d-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfe0d-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cfe0d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfe0d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe0d-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfe0d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cfe0d-141">Header</span><span class="sxs-lookup"><span data-stu-id="cfe0d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfe0d-142"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe0d-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfe0d-143">IDL</span><span class="sxs-lookup"><span data-stu-id="cfe0d-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cfe0d-144"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cfe0d-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="cfe0d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cfe0d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfe0d-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfe0d-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="cfe0d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfe0d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe0d-148">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cfe0d-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cfe0d-149">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="cfe0d-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

