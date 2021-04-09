---
title: INapEnforcementClientConnection2-Schnittstelle (napforcementclient. h)
description: Ermöglicht die clientverbindungsverwaltung. | INapEnforcementClientConnection2-Schnittstelle (napforcementclient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2-Schnittstelle NAP
- INapEnforcementClientConnection2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869743"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="9829f-106">INapEnforcementClientConnection2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9829f-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="9829f-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9829f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9829f-108">Der **INapEnforcementClientConnection2** stellt Methoden bereit, die die Client Verbindungs Verwaltung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9829f-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="9829f-109">Diese Schnittstelle erbt alle Methoden von [**inapenforcementclientconnection**](inapenforcementclientconnection.md) und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9829f-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="9829f-110">Member</span><span class="sxs-lookup"><span data-stu-id="9829f-110">Members</span></span>

<span data-ttu-id="9829f-111">Die **INapEnforcementClientConnection2** -Schnittstelle erbt von [**inapenforcementclientconnection**](inapenforcementclientconnection.md).</span><span class="sxs-lookup"><span data-stu-id="9829f-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="9829f-112">**INapEnforcementClientConnection2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9829f-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="9829f-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9829f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9829f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="9829f-114">Methods</span></span>

<span data-ttu-id="9829f-115">Die **INapEnforcementClientConnection2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9829f-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="9829f-116">Methode</span><span class="sxs-lookup"><span data-stu-id="9829f-116">Method</span></span>                                                                                                              | <span data-ttu-id="9829f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9829f-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="9829f-118">**INapEnforcementClientConnection2:: getinstalledshvs**</span><span class="sxs-lookup"><span data-stu-id="9829f-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="9829f-119">Wird verwendet, um die IDs der installierten SHVs für den Client abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9829f-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="9829f-120">**INapEnforcementClientConnection2:: getisolationinfoex**</span><span class="sxs-lookup"><span data-stu-id="9829f-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="9829f-121">Wird verwendet, um die Isolations Informationen für den Client zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9829f-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="9829f-122">**INapEnforcementClientConnection2:: setinstalledshvs**</span><span class="sxs-lookup"><span data-stu-id="9829f-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="9829f-123">Wird von NAPAgent verwendet, um die installierten SHV-IDs für den Client festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9829f-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="9829f-124">**INapEnforcementClientConnection2::/tisolationinfoex**</span><span class="sxs-lookup"><span data-stu-id="9829f-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="9829f-125">Wird von NAPAgent verwendet, um die Isolations Informationen für den Client festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9829f-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9829f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9829f-126">Requirements</span></span>



| <span data-ttu-id="9829f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9829f-127">Requirement</span></span> | <span data-ttu-id="9829f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9829f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9829f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9829f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9829f-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9829f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9829f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9829f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9829f-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9829f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9829f-133">Header</span><span class="sxs-lookup"><span data-stu-id="9829f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9829f-134"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9829f-135">IDL</span><span class="sxs-lookup"><span data-stu-id="9829f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9829f-136"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="9829f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9829f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9829f-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9829f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9829f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9829f-140">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="9829f-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="9829f-141">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9829f-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9829f-142">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="9829f-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





