---
description: Gibt eine hohe, mittlere oder geringe Auswirkung auf ein Gerät an, auf dem ein veralteter Betriebssystem ausgeführt wird.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Updateimpactlevel-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372873"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="e89df-103">Updateimpactlevel-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e89df-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="e89df-104">Gibt eine hohe, mittlere oder geringe Auswirkung auf ein Gerät an, auf dem ein veralteter Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e89df-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="e89df-105">Diese Enumeration wird in der Regel von [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) -Strukturen verwendet, die wiederum innerhalb des zurückgegebenen [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) -Werts von [**gedesupdateassessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)geschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="e89df-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="e89df-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e89df-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="e89df-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e89df-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e89df-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**Updateimpactlevel \_ Keine**</span><span class="sxs-lookup"><span data-stu-id="e89df-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="e89df-109">Es gibt keine vorhersehbaren Auswirkungen auf Ihr Gerät.</span><span class="sxs-lookup"><span data-stu-id="e89df-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="e89df-110">Dies kann darauf zurückzuführen sein, dass das Gerät auf dem neuesten Stand ist oder nicht auf dem neuesten Stand ist, weil das Gerät seine Windows Update für Geschäfts zurückstellungs Zeiträume berücksichtigt oder veraltet ist, aber den **daysouumfdate** -Schwellenwert noch nicht erreicht hat, um eine höhere Auswirkung zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="e89df-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="e89df-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**Updateimpactlevel \_ niedrig**</span><span class="sxs-lookup"><span data-stu-id="e89df-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="e89df-112">Auf dem Gerät wird nicht das neueste Betriebssystem, sondern ein aktuellstes Update ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e89df-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="e89df-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**Updateimpactlevel \_ Mittel**</span><span class="sxs-lookup"><span data-stu-id="e89df-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="e89df-114">Auf dem Gerät wird das neueste Betriebssystem ausgeführt, aber es wird ein moderater neueres Update ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e89df-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="e89df-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**Updateimpactlevel \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="e89df-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="e89df-116">Das Gerät ist seit längerer Zeit veraltet.</span><span class="sxs-lookup"><span data-stu-id="e89df-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="e89df-117">Dieses Gerät weist möglicherweise Sicherheitsrisiken auf und enthält möglicherweise wichtige Korrekturen, mit denen Windows besser ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e89df-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="e89df-118">Wenn auf einem Gerät eine Version von Windows ausgeführt wird, die nicht mehr unterstützt wird, wird **updateimpactlevel \_ High** immer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e89df-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e89df-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e89df-119">Remarks</span></span>

<span data-ttu-id="e89df-120">Wenn [**gedesupdateassessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) aufgerufen wird, wird eine [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) -Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e89df-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="e89df-121">Innerhalb der-Struktur gibt es einen " **Assessment mentforcurrent** " und " **Assessment mentforuptodate**".</span><span class="sxs-lookup"><span data-stu-id="e89df-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="e89df-122">Beide sind [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e89df-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="e89df-123">Beide Member verfügen über eine **updateimpactlevel** -Enumeration, die eine hohe, mittlere, geringe oder keine Auswirkung für ein Gerät mit einem veralteten Betriebssystem angibt.</span><span class="sxs-lookup"><span data-stu-id="e89df-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="e89df-124">Diese Ebenen werden durch den Wert von **daysoudef Date** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e89df-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e89df-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e89df-125">Requirements</span></span>



| <span data-ttu-id="e89df-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e89df-126">Requirement</span></span> | <span data-ttu-id="e89df-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e89df-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e89df-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e89df-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e89df-129">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e89df-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e89df-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e89df-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e89df-131">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e89df-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e89df-132">IDL</span><span class="sxs-lookup"><span data-stu-id="e89df-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e89df-133"><dt>Waasapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e89df-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




