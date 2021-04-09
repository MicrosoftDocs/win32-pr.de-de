---
title: Inapcertrelyingparty-Schnittstelle (napcertrelyingparty. h)
description: Zertifikat abhängige Seiten müssen für die Kommunikation mit dem NAPAgent verwenden.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- Inapcertrelyingparty-Schnittstelle NAP
- Inapcertrelyingparty-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040779"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="77eb6-105">Inapcertrelyingparty-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="77eb6-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="77eb6-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77eb6-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="77eb6-107">Die **inapcertrelyingparty** -Schnittstelle stellt Methoden bereit, die von Zertifikat vertrauenden Seiten für die Kommunikation mit dem NAPAgent verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="77eb6-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="77eb6-108">Member</span><span class="sxs-lookup"><span data-stu-id="77eb6-108">Members</span></span>

<span data-ttu-id="77eb6-109">Die **inapcertrelyingparty** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="77eb6-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77eb6-110">**Inapcertrelyingparty** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="77eb6-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="77eb6-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="77eb6-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77eb6-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="77eb6-112">Methods</span></span>

<span data-ttu-id="77eb6-113">Die **inapcertrelyingparty** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="77eb6-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="77eb6-114">Methode</span><span class="sxs-lookup"><span data-stu-id="77eb6-114">Method</span></span>                                                                                                        | <span data-ttu-id="77eb6-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77eb6-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="77eb6-116">**Inapcertrelyingparty:: getabonbedrelyingparties**</span><span class="sxs-lookup"><span data-stu-id="77eb6-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="77eb6-117">Ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.</span><span class="sxs-lookup"><span data-stu-id="77eb6-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="77eb6-118">**Inapcertrelyingparty:: abonnebecertbygroup**</span><span class="sxs-lookup"><span data-stu-id="77eb6-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="77eb6-119">Abonniert einen bereits registrierten Integritäts Zertifikat Server (HCS).</span><span class="sxs-lookup"><span data-stu-id="77eb6-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="77eb6-120">**Inapcertrelyingparty:: unabonnebecertbygroup**</span><span class="sxs-lookup"><span data-stu-id="77eb6-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="77eb6-121">Kündigen von einem HCS-Server.</span><span class="sxs-lookup"><span data-stu-id="77eb6-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="77eb6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77eb6-122">Requirements</span></span>



| <span data-ttu-id="77eb6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77eb6-123">Requirement</span></span> | <span data-ttu-id="77eb6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="77eb6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77eb6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77eb6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="77eb6-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77eb6-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77eb6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77eb6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="77eb6-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77eb6-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="77eb6-129">Header</span><span class="sxs-lookup"><span data-stu-id="77eb6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="77eb6-130"><dt>Napcertrelyingparty. h</dt></span><span class="sxs-lookup"><span data-stu-id="77eb6-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="77eb6-131">IDL</span><span class="sxs-lookup"><span data-stu-id="77eb6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77eb6-132"><dt>Napcertrelyingparty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77eb6-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77eb6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77eb6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77eb6-134">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="77eb6-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="77eb6-135">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="77eb6-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

