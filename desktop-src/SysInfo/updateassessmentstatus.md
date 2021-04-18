---
description: Hier wird beschrieben, wie das Betriebssystem auf einem Gerät auf dem neuesten Stand ist.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Updateassessment mentstatus-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347224"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="b02f9-103">Updateassessment mentstatus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b02f9-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="b02f9-104">Hier wird beschrieben, wie das Betriebssystem auf einem Gerät auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="b02f9-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="b02f9-105">**Updategutamentstatus** wird von den-Strukturen " [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) " und " [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) " in den Elementen " **Assessment mentforcurrent**", " **bewermentforuptodate**" und " **SecurityStatus** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="b02f9-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="b02f9-106">Es wird genau eine Konstante zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b02f9-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b02f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b02f9-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="b02f9-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b02f9-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b02f9-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**Updategutamentstatus \_ Neueste** Version</span><span class="sxs-lookup"><span data-stu-id="b02f9-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-110">Dieses Ergebnis in " **bewermentforcurrent** " impliziert, dass sich das Gerät auf dem neuesten Feature Update und Qualitäts Update befindet, das für dieses Gerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b02f9-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="b02f9-111">In " **bewermentforuptodate**" bedeutet das, dass das Gerät das aktuellste Qualitäts Update für die Windows-Version ist, die es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b02f9-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**Updategutamentstatus \_ Notlatestsoftrestriction**</span><span class="sxs-lookup"><span data-stu-id="b02f9-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-113">Das aktuellste Funktions Update wurde aufgrund einer Soft-Einschränkung nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="b02f9-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="b02f9-114">Wenn eine weiche Einschränkung für ein Update festgelegt wurde, wird das Update nicht automatisch installiert. ein Benutzer muss den Download innerhalb der Update-UX selbst initiieren.</span><span class="sxs-lookup"><span data-stu-id="b02f9-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="b02f9-115">Dieser Status gilt nur für " **bewermentforcurrent**".</span><span class="sxs-lookup"><span data-stu-id="b02f9-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**Updategutamentstatus \_ Notlatesthardrestriction**</span><span class="sxs-lookup"><span data-stu-id="b02f9-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-117">Das aktuellste Funktions Update wurde aufgrund einer festen Einschränkung nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="b02f9-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="b02f9-118">Wenn eine feste Einschränkung für ein Update festgelegt wurde, kann das Update nicht auf das Gerät angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02f9-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="b02f9-119">Dieser Status gilt nur für " **bewermentforcurrent**".</span><span class="sxs-lookup"><span data-stu-id="b02f9-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**Updategutamentstatus \_ Notlatestendof Support**</span><span class="sxs-lookup"><span data-stu-id="b02f9-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-121">Das Gerät befindet sich nicht auf dem neuesten Update, da das Feature-Update des Geräts von Microsoft nicht mehr unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b02f9-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="b02f9-122">Wenn Microsoft eine Featureversion nicht mehr unterstützt, wird dieser Status sowohl für " **bewermentforcurrent** " als auch für " **bewermentforuptodate**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b02f9-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="b02f9-123">Wenn **updategutamentstatus \_ notlatestendofsupport** zurückgegeben wird, ist **updateimpactlevel** der Bewertung immer **updateimpactlevel \_ hoch**.</span><span class="sxs-lookup"><span data-stu-id="b02f9-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="b02f9-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**Updategutamentstatus \_ Notlatestservicingtrain**</span><span class="sxs-lookup"><span data-stu-id="b02f9-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-125">Das Gerät befindet sich nicht im aktuellen Featureupdate, da der Wartungsplan des Geräts die Aktualisierung auf das neueste Featureupdate einschränkt.</span><span class="sxs-lookup"><span data-stu-id="b02f9-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="b02f9-126">Beispiel: Wenn ein Gerät on Current Branch for Business (CBB) ist und ein neues Funktions Update für Current Branch (CB) veröffentlicht wurde, wird dieses zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b02f9-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="b02f9-127">Dieser Status gilt nur für " **bewermentforcurrent**".</span><span class="sxs-lookup"><span data-stu-id="b02f9-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**Updategutamentstatus \_ Notlatestdeferredfeature**</span><span class="sxs-lookup"><span data-stu-id="b02f9-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-129">Das aktuellste Featureupdate wurde nicht installiert, da es die zurückstellungs Richtlinie für das Windows Update for Business Feature Update des Geräts ist.</span><span class="sxs-lookup"><span data-stu-id="b02f9-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="b02f9-130">Beim Bestimmen von **daysoutof** werden zurückstellungs Richtlinien berücksichtigt. **daysoudef** beginnt nicht mit dem Inkrementieren, bis der zurückstellungs Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="b02f9-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="b02f9-131">Dieser Status gilt nur für " **bewermentforcurrent**".</span><span class="sxs-lookup"><span data-stu-id="b02f9-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**Updategutamentstatus \_ Notlatestdeferredquality**</span><span class="sxs-lookup"><span data-stu-id="b02f9-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-133">Das Gerät befindet sich nicht auf dem neuesten Qualitäts Update aufgrund der Windows Update des Geräts für die zurückstellungs Richtlinie für Geschäfts Qualitäts Updates.</span><span class="sxs-lookup"><span data-stu-id="b02f9-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="b02f9-134">Beim Bestimmen von **daysoutof** werden zurückstellungs Richtlinien berücksichtigt. **daysoudef** beginnt nicht mit dem Inkrementieren, bis der zurückstellungs Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="b02f9-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**Updategutamentstatus \_ Notlatestpausedfeature**</span><span class="sxs-lookup"><span data-stu-id="b02f9-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-136">Das Gerät befindet sich nicht auf dem neuesten Feature-Update, weil das Gerät über angehaltene Featureupdates verfügt.</span><span class="sxs-lookup"><span data-stu-id="b02f9-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="b02f9-137">Ob ein Gerät angehalten wurde, wird nicht in die Berechnung von **daysouumf Date** einbezogen.</span><span class="sxs-lookup"><span data-stu-id="b02f9-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="b02f9-138">Dieser Status gilt nur für " **bewermentforcurrent**".</span><span class="sxs-lookup"><span data-stu-id="b02f9-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**Updategutamentstatus \_ Notlatestpausedquality**</span><span class="sxs-lookup"><span data-stu-id="b02f9-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-140">Das Gerät befindet sich nicht auf dem neuesten Qualitäts Update, weil das Gerät über angehaltene Qualitäts Updates verfügt.</span><span class="sxs-lookup"><span data-stu-id="b02f9-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="b02f9-141">Ob ein Gerät angehalten wurde, wird nicht in die Berechnung von **daysouumf Date** einbezogen.</span><span class="sxs-lookup"><span data-stu-id="b02f9-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="b02f9-142">**daysoudef** ist nicht maßgeblich, ob ein Gerät in seiner Berechnung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="b02f9-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**Updategutamentstatus \_ Notlatestmanaged**</span><span class="sxs-lookup"><span data-stu-id="b02f9-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-144">Das Gerät befindet sich nicht auf dem neuesten Update, da die Genehmigung von Updates nicht über Windows Update erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b02f9-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**Updategutamentstatus \_ Notlatestunknown**</span><span class="sxs-lookup"><span data-stu-id="b02f9-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-146">Das Gerät befindet sich nicht auf dem neuesten Update, weil der Grund dafür nicht durch die Bewertung bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b02f9-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="b02f9-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**Updategutamentstatus \_ Notlatesttargetedversion**</span><span class="sxs-lookup"><span data-stu-id="b02f9-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b02f9-148">Das Gerät befindet sich nicht im aktuellen Featureupdate aufgrund der Richtlinie für das Windows Update für die Geschäftsziel Version des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b02f9-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="b02f9-149">Bei dieser Richtlinie wird das Gerät auf der Zielversion der Funktions Version belassen.</span><span class="sxs-lookup"><span data-stu-id="b02f9-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b02f9-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b02f9-150">Remarks</span></span>

<span data-ttu-id="b02f9-151">Diese Enumeration wird am häufigsten mit den Strukturen [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) und [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) verwendet, die wiederum mit der [**gedesupdateassessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) -Methode für [**iwaasassessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02f9-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="b02f9-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b02f9-152">Requirements</span></span>



| <span data-ttu-id="b02f9-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b02f9-153">Requirement</span></span> | <span data-ttu-id="b02f9-154">Wert</span><span class="sxs-lookup"><span data-stu-id="b02f9-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b02f9-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b02f9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b02f9-156">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02f9-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b02f9-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b02f9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b02f9-158">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02f9-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b02f9-159">IDL</span><span class="sxs-lookup"><span data-stu-id="b02f9-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b02f9-160"><dt>Waasapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b02f9-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




