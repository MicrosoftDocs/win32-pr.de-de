---
title: Updatefromds-Methode der MicrosoftDNS_Zone-Klasse
description: Die updatefromds-Methode erzwingt ein Update der Zone aus dem Verzeichnisdienst (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- Updatefromds-Methode (DNS)
- Updatefromds-Methode, DNS, MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, updatefromds-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106569"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="f2707-106">Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="f2707-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="f2707-107">Die **updatefromds** -Methode erzwingt ein Update der Zone aus dem Verzeichnisdienst (DS).</span><span class="sxs-lookup"><span data-stu-id="f2707-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2707-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2707-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="f2707-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2707-109">Parameters</span></span>

<span data-ttu-id="f2707-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f2707-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2707-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2707-111">Return value</span></span>

<span data-ttu-id="f2707-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f2707-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2707-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2707-113">Remarks</span></span>

<span data-ttu-id="f2707-114">Damit diese Methode erfolgreich ausgeführt werden kann, muss zonetype NULL sein, und die Zone muss auf dem DS gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f2707-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2707-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2707-115">Requirements</span></span>



| <span data-ttu-id="f2707-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2707-116">Requirement</span></span> | <span data-ttu-id="f2707-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f2707-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2707-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2707-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2707-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f2707-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f2707-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2707-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2707-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2707-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f2707-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2707-122">Namespace</span></span><br/>                | <span data-ttu-id="f2707-123">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f2707-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f2707-124">MOF</span><span class="sxs-lookup"><span data-stu-id="f2707-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2707-125"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f2707-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2707-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2707-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2707-127">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="f2707-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="f2707-128">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="f2707-129">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="f2707-130">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="f2707-131">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="f2707-132">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="f2707-133">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="f2707-134">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="f2707-135">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="f2707-136">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="f2707-137">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2707-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





