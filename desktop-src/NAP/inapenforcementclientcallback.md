---
title: Inapenforcementclientcallback-Schnittstelle (napforcementclient. h)
description: Erzwingungs Clients müssen implementieren, damit der NAPAgent mit Ihnen kommunizieren kann.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- Inapenforcementclientcallback-Schnittstelle NAP
- Inapenforcementclientcallback-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342486"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="bc9bb-105">Inapenforcementclientcallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bc9bb-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="bc9bb-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bc9bb-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bc9bb-107">Die **inapenforcementclientcallback** -Schnittstelle stellt Rückruf Methoden bereit, die von Erzwingungs Clients implementiert werden müssen, damit der NAPAgent mit Ihnen kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="bc9bb-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="bc9bb-108">Member</span><span class="sxs-lookup"><span data-stu-id="bc9bb-108">Members</span></span>

<span data-ttu-id="bc9bb-109">Die **inapenforcementclientcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bc9bb-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bc9bb-110">**Inapenforcementclientcallback** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bc9bb-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="bc9bb-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="bc9bb-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bc9bb-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="bc9bb-112">Methods</span></span>

<span data-ttu-id="bc9bb-113">Die **inapenforcementclientcallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bc9bb-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="bc9bb-114">Methode</span><span class="sxs-lookup"><span data-stu-id="bc9bb-114">Method</span></span>                                                                                                         | <span data-ttu-id="bc9bb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc9bb-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="bc9bb-116">**Inapenforcementclientcallback:: GetConnections**</span><span class="sxs-lookup"><span data-stu-id="bc9bb-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="bc9bb-117">Wird vom NAPAgent zum Abrufen von Verbindungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc9bb-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="bc9bb-118">**Inapenforcementclientcallback:: notifysohchange**</span><span class="sxs-lookup"><span data-stu-id="bc9bb-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="bc9bb-119">Wird vom NAPAgent verwendet, um den Erzwingungs Client über SoH-Änderungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="bc9bb-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bc9bb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc9bb-120">Requirements</span></span>



| <span data-ttu-id="bc9bb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc9bb-121">Requirement</span></span> | <span data-ttu-id="bc9bb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bc9bb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9bb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc9bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9bb-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc9bb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc9bb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc9bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9bb-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc9bb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc9bb-127">Header</span><span class="sxs-lookup"><span data-stu-id="bc9bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc9bb-128"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc9bb-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc9bb-129">IDL</span><span class="sxs-lookup"><span data-stu-id="bc9bb-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc9bb-130"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc9bb-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 

