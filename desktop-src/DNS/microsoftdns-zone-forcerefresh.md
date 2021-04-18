---
title: ForceRefresh-Methode der MicrosoftDNS_Zone-Klasse
description: Die forceRefresh-Methode erzwingt ein Update des sekundären DNS-Servers vom Master Server.
ms.assetid: 8dde1703-53c3-4d1e-bfb3-f6d5d1666740
keywords:
- ForceRefresh-Methode (DNS)
- ForceRefresh-Methode, DNS, MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, forceRefresh-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ForceRefresh
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85390230b0a0852ee479bc8b7e396972f6e69080
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341085"
---
# <a name="forcerefresh-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="83469-106">ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="83469-106">ForceRefresh method of the MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="83469-107">Dieser Artikel enthält Verweise auf den Begriff Master Server, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="83469-107">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="83469-108">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="83469-108">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="83469-109">Die **forceRefresh** -Methode erzwingt ein Update des sekundären DNS-Servers vom Master Server.</span><span class="sxs-lookup"><span data-stu-id="83469-109">The **ForceRefresh** method forces an update of the secondary DNS Server from the master server.</span></span>

## <a name="syntax"></a><span data-ttu-id="83469-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="83469-110">Syntax</span></span>


```mof
void ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="83469-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="83469-111">Parameters</span></span>

<span data-ttu-id="83469-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="83469-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83469-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83469-113">Return value</span></span>

<span data-ttu-id="83469-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="83469-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="83469-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83469-115">Requirements</span></span>



| <span data-ttu-id="83469-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83469-116">Requirement</span></span> | <span data-ttu-id="83469-117">Wert</span><span class="sxs-lookup"><span data-stu-id="83469-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83469-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83469-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83469-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="83469-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="83469-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83469-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83469-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83469-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="83469-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="83469-122">Namespace</span></span><br/>                | <span data-ttu-id="83469-123">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="83469-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="83469-124">MOF</span><span class="sxs-lookup"><span data-stu-id="83469-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83469-125"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="83469-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83469-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83469-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83469-127">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="83469-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="83469-128">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="83469-129">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="83469-130">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="83469-131">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-131">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="83469-132">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-132">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="83469-133">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-133">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="83469-134">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-134">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="83469-135">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-135">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="83469-136">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-136">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="83469-137">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="83469-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





