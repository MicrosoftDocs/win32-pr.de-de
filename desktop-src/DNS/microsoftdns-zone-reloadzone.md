---
title: Reloadzone-Methode der MicrosoftDNS_Zone-Klasse
description: Mit der reloadzone-Methode wird die DNS-Zone aus der Datenbank erneut geladen.
ms.assetid: 9fb3c216-563c-4603-a29a-27627ac644d8
keywords:
- Reloadzone-Methode (DNS)
- Reloadzone-Methode (DNS), MicrosoftDNS_Zone-Klasse
- MicrosoftDNS_Zone-Klasse DNS, reloadzone-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ReloadZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e22d9becc5084407267e75d713082ce5dcbb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956788"
---
# <a name="reloadzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="06566-106">Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="06566-106">ReloadZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="06566-107">Mit der **reloadzone** -Methode wird die DNS-Zone aus der Datenbank erneut geladen.</span><span class="sxs-lookup"><span data-stu-id="06566-107">The **ReloadZone** method reloads the DNS Zone from its database.</span></span>

## <a name="syntax"></a><span data-ttu-id="06566-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06566-108">Syntax</span></span>


```mof
void ReloadZone();
```



## <a name="parameters"></a><span data-ttu-id="06566-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="06566-109">Parameters</span></span>

<span data-ttu-id="06566-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="06566-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06566-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06566-111">Return value</span></span>

<span data-ttu-id="06566-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="06566-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06566-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06566-113">Requirements</span></span>



| <span data-ttu-id="06566-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06566-114">Requirement</span></span> | <span data-ttu-id="06566-115">Wert</span><span class="sxs-lookup"><span data-stu-id="06566-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06566-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06566-116">Minimum supported client</span></span><br/> | <span data-ttu-id="06566-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="06566-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="06566-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06566-118">Minimum supported server</span></span><br/> | <span data-ttu-id="06566-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06566-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06566-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="06566-120">Namespace</span></span><br/>                | <span data-ttu-id="06566-121">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="06566-121">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="06566-122">MOF</span><span class="sxs-lookup"><span data-stu-id="06566-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06566-123"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="06566-123"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06566-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06566-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06566-125">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="06566-125">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="06566-126">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-126">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="06566-127">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-127">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="06566-128">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-128">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="06566-129">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-129">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="06566-130">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-130">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="06566-131">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-131">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="06566-132">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-132">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="06566-133">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-133">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="06566-134">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-134">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="06566-135">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="06566-135">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





