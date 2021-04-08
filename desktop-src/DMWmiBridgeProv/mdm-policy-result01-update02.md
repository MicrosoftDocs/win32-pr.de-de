---
title: MDM_Policy_Result01_Update02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Update02-Klasse stellt die verfügbaren Update Richtlinien dar.
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- MDM_Policy_Result01_Update02-Klasse
- MDM_Policy_Result01_Update02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949454"
---
# <a name="mdm_policy_result01_update02-class"></a><span data-ttu-id="3daa6-105">MDM- \_ Richtlinie \_ Result01 \_ Update02-Klasse</span><span class="sxs-lookup"><span data-stu-id="3daa6-105">MDM\_Policy\_Result01\_Update02 class</span></span>

<span data-ttu-id="3daa6-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="3daa6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3daa6-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="3daa6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3daa6-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Update02** -Klasse stellt die verfügbaren Update Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="3daa6-108">The **MDM\_Policy\_Result01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="3daa6-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="3daa6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3daa6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3daa6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="3daa6-111">Member</span><span class="sxs-lookup"><span data-stu-id="3daa6-111">Members</span></span>

<span data-ttu-id="3daa6-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Update02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3daa6-112">The **MDM\_Policy\_Result01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="3daa6-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3daa6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3daa6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3daa6-114">Properties</span></span>

<span data-ttu-id="3daa6-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Update02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3daa6-115">The **MDM\_Policy\_Result01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3daa6-116">Activehoursend</span><span class="sxs-lookup"><span data-stu-id="3daa6-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-119">Activehoursmaxrange</span><span class="sxs-lookup"><span data-stu-id="3daa6-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-122">Activehoursstart</span><span class="sxs-lookup"><span data-stu-id="3daa6-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-125">Allowautoupdate</span><span class="sxs-lookup"><span data-stu-id="3daa6-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-128">Allowautowindowsupdatedownloadovermeterednetwork</span><span class="sxs-lookup"><span data-stu-id="3daa6-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-131">Allowmuupdateservice</span><span class="sxs-lookup"><span data-stu-id="3daa6-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-134">Allownonmicrosoftsignetdupdate</span><span class="sxs-lookup"><span data-stu-id="3daa6-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="3daa6-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-140">Autorestartdeadlineperiodindays</span><span class="sxs-lookup"><span data-stu-id="3daa6-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-143">Autorestartnotificationschedule</span><span class="sxs-lookup"><span data-stu-id="3daa6-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-146">Autorestartrequirednotificationentlassung</span><span class="sxs-lookup"><span data-stu-id="3daa6-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="3daa6-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="3daa6-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-155">Deferqualityupdatesperiodindays</span><span class="sxs-lookup"><span data-stu-id="3daa6-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="3daa6-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-161">Deferupgradezperiod</span><span class="sxs-lookup"><span data-stu-id="3daa6-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-164">Erkenctionfrequency</span><span class="sxs-lookup"><span data-stu-id="3daa6-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-167">Disabledualscan</span><span class="sxs-lookup"><span data-stu-id="3daa6-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-170">Engagedrestartstichtag</span><span class="sxs-lookup"><span data-stu-id="3daa6-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-173">Engagedrestartnoozeschedule</span><span class="sxs-lookup"><span data-stu-id="3daa6-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-174">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-176">Engagedrestarttransitionschedule</span><span class="sxs-lookup"><span data-stu-id="3daa6-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-177">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-179">Excluabwudriversinqualityupdate</span><span class="sxs-lookup"><span data-stu-id="3daa6-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-180">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-182">Fillemptycontenturls</span><span class="sxs-lookup"><span data-stu-id="3daa6-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-185">Ignoremoappdownloadlimit</span><span class="sxs-lookup"><span data-stu-id="3daa6-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-186">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-188">Ignoremoupdatedownloadlimit</span><span class="sxs-lookup"><span data-stu-id="3daa6-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3daa6-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3daa6-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3daa6-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3daa6-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-194">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3daa6-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3daa6-195">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="3daa6-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="3daa6-196">Für diese Klasse ist die Zeichenfolge "Update".</span><span class="sxs-lookup"><span data-stu-id="3daa6-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="3daa6-197">Managepreviewbuilds</span><span class="sxs-lookup"><span data-stu-id="3daa6-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-198">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3daa6-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3daa6-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3daa6-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3daa6-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-203">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3daa6-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3daa6-204">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="3daa6-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="3daa6-205">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="3daa6-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="3daa6-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="3daa6-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="3daa6-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-212">Pausefeatureupdatesstarttime</span><span class="sxs-lookup"><span data-stu-id="3daa6-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3daa6-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="3daa6-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-216">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-218">Pausequalityupdatesstarttime</span><span class="sxs-lookup"><span data-stu-id="3daa6-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3daa6-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-221">Phoneupdaterestrictions</span><span class="sxs-lookup"><span data-stu-id="3daa6-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-222">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="3daa6-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-225">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="3daa6-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-228">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="3daa6-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-231">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-233">Scheduledinstalleveryweek</span><span class="sxs-lookup"><span data-stu-id="3daa6-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-234">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-236">Scheduledinstallfirstweek</span><span class="sxs-lookup"><span data-stu-id="3daa6-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-237">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-239">Scheduledinstallfourthweek</span><span class="sxs-lookup"><span data-stu-id="3daa6-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-240">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-242">Scheduledinstallsecondweek</span><span class="sxs-lookup"><span data-stu-id="3daa6-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-243">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-245">Scheduledinstallthirdweek</span><span class="sxs-lookup"><span data-stu-id="3daa6-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-246">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="3daa6-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-249">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-251">Scheduleimminentrestartwarning</span><span class="sxs-lookup"><span data-stu-id="3daa6-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-252">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-254">Schedulerestartwarning</span><span class="sxs-lookup"><span data-stu-id="3daa6-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-255">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-257">Setautoriestartnotificationdeaktivieren</span><span class="sxs-lookup"><span data-stu-id="3daa6-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-258">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-260">"".</span><span class="sxs-lookup"><span data-stu-id="3daa6-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-261">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3daa6-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-263">Updateserviceurl</span><span class="sxs-lookup"><span data-stu-id="3daa6-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3daa6-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3daa6-266">Updateserviceurlalternate</span><span class="sxs-lookup"><span data-stu-id="3daa6-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3daa6-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3daa6-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3daa6-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3daa6-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3daa6-269">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3daa6-269">Requirements</span></span>



| <span data-ttu-id="3daa6-270">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3daa6-270">Requirement</span></span> | <span data-ttu-id="3daa6-271">Wert</span><span class="sxs-lookup"><span data-stu-id="3daa6-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3daa6-272">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3daa6-272">Minimum supported client</span></span><br/> | <span data-ttu-id="3daa6-273">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3daa6-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3daa6-274">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3daa6-274">Minimum supported server</span></span><br/> | <span data-ttu-id="3daa6-275">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3daa6-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3daa6-276">Namespace</span><span class="sxs-lookup"><span data-stu-id="3daa6-276">Namespace</span></span><br/>                | <span data-ttu-id="3daa6-277">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3daa6-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3daa6-278">MOF</span><span class="sxs-lookup"><span data-stu-id="3daa6-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3daa6-279"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3daa6-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3daa6-280">DLL</span><span class="sxs-lookup"><span data-stu-id="3daa6-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3daa6-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3daa6-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3daa6-282">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3daa6-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3daa6-283">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="3daa6-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

