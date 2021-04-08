---
title: Iadsnametranslation-Eigenschaften Methoden (IADs. h)
description: Legt die chasereferral-Eigenschaft fest.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Iadsnametranslation-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956907"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="8699c-104">Iadsnametranslation-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="8699c-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="8699c-105">Die Property-Methode der [**iadsnametranslation**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) -Schnittstelle legt die **chasereferral** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="8699c-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="8699c-106">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8699c-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8699c-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8699c-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8699c-108">**Chasereferral**</span><span class="sxs-lookup"><span data-stu-id="8699c-108">**ChaseReferral**</span></span>
<span data-ttu-id="8699c-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8699c-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="8699c-110">Optionen für die Verweis Verfolgung gemäß der Definition in [**ADS \_ Chase \_ referenrals \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span><span class="sxs-lookup"><span data-stu-id="8699c-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="8699c-111">Wenn die verweisverfolgung festgelegt ist, wird die namens Übersetzung für Objekte durchgeführt, die nicht zu diesem Verzeichnis gehören und die von der Verweis Verfolgung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8699c-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="8699c-112">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8699c-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="8699c-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="8699c-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="8699c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8699c-114">Remarks</span></span>

<span data-ttu-id="8699c-115">Die verweiserverfolgungs-Optionen gelten nur, wenn Sie [**iadsnametranslation:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) und [**iadsnametranslation:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)verwenden.</span><span class="sxs-lookup"><span data-stu-id="8699c-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="8699c-116">Die Funktion ist nicht in [**iadsnametranslation::**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) Stex oder [**iadsnametranslation:: Getex**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8699c-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="8699c-117">Die [**iadsnametranslation**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) -Schnittstelle verfügt über eine partielle Implementierung von [**ADS- \_ \_ Verweigerungs verweisen \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) über die **chasereferral** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8699c-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="8699c-118">Wenn die **chasereferral** -Eigenschaft auf 0 (null) festgelegt ist, entspricht Sie der Angabe von **ADS- \_ \_ Verweigerungs verweisen \_ nie** (0).</span><span class="sxs-lookup"><span data-stu-id="8699c-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="8699c-119">Wenn ein Wert ungleich 0 (null) verwendet wird, entspricht er dem Angeben von ADS-verweisverweisverweisen **\_ \_ \_ immer** (0x60).</span><span class="sxs-lookup"><span data-stu-id="8699c-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="8699c-120">**Iadsnametranslation** implementiert nicht die " **ADS \_ Chase \_ referenrals unter \_ geordnete** (0x20)" oder " **ADS \_ Chase \_ verweirals \_** "-Option "externe (0x40)"-Optionen.</span><span class="sxs-lookup"><span data-stu-id="8699c-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="8699c-121">Die Standardeinstellung für die Weiterleitungs Verfolgung ist aktiviert (ADS-verweisverweisverweise **\_ \_ \_ immer**).</span><span class="sxs-lookup"><span data-stu-id="8699c-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="8699c-122">Ohne eine verweisverfolgung kann eine namens Übersetzung für die Objekte ausgeführt werden, die sich nur auf dem verbundenen Verzeichnisserver befinden.</span><span class="sxs-lookup"><span data-stu-id="8699c-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="8699c-123">Wenn Sie nicht sicher sind, ob sich das relevante Objekt auf dem angegebenen Server befindet, sollten Sie diese Eigenschaft auf " **ADS \_ Chase- \_ Verweise \_ immer**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="8699c-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8699c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8699c-124">Requirements</span></span>



| <span data-ttu-id="8699c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8699c-125">Requirement</span></span> | <span data-ttu-id="8699c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8699c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8699c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8699c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8699c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8699c-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8699c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8699c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8699c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8699c-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8699c-131">Header</span><span class="sxs-lookup"><span data-stu-id="8699c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8699c-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8699c-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8699c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8699c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8699c-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8699c-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8699c-135">IID</span><span class="sxs-lookup"><span data-stu-id="8699c-135">IID</span></span><br/>                      | <span data-ttu-id="8699c-136">IID \_ iadsnametranslation ist als B1B272A3-3625-11d1-A3A4-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="8699c-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="8699c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8699c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8699c-138">**Werbung für Werbung- \_ \_ Verweigerungen \_**</span><span class="sxs-lookup"><span data-stu-id="8699c-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="8699c-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="8699c-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="8699c-140">**Iadsnametranslation:: Get**</span><span class="sxs-lookup"><span data-stu-id="8699c-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="8699c-141">**Iadsnametranslation:: Getex**</span><span class="sxs-lookup"><span data-stu-id="8699c-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="8699c-142">**Iadsnametranslation:: Set**</span><span class="sxs-lookup"><span data-stu-id="8699c-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="8699c-143">**Iadsnametranslation::-TeX**</span><span class="sxs-lookup"><span data-stu-id="8699c-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="8699c-144">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="8699c-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





