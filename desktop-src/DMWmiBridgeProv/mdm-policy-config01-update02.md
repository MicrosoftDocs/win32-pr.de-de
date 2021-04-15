---
title: MDM_Policy_Config01_Update02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Update02-Klasse stellt die verfügbaren Update Richtlinien dar.
ms.assetid: 7324912c-7ac5-42fd-baee-f7e2d81de023
keywords:
- MDM_Policy_Config01_Update02-Klasse
- MDM_Policy_Config01_Update02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02.InstanceID
- MDM_Policy_Config01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3044fc527fd23d49fac383dc25778d3a978b2788
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476917"
---
# <a name="mdm_policy_config01_update02-class"></a><span data-ttu-id="1edc8-105">MDM- \_ Richtlinie \_ Config01 \_ Update02-Klasse</span><span class="sxs-lookup"><span data-stu-id="1edc8-105">MDM\_Policy\_Config01\_Update02 class</span></span>

<span data-ttu-id="1edc8-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1edc8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1edc8-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1edc8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1edc8-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Update02** -Klasse stellt die verfügbaren Update Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="1edc8-108">The **MDM\_Policy\_Config01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="1edc8-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1edc8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1edc8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1edc8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Update02
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

## <a name="members"></a><span data-ttu-id="1edc8-111">Member</span><span class="sxs-lookup"><span data-stu-id="1edc8-111">Members</span></span>

<span data-ttu-id="1edc8-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Update02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1edc8-112">The **MDM\_Policy\_Config01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="1edc8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1edc8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1edc8-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1edc8-114">Properties</span></span>

<span data-ttu-id="1edc8-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Update02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1edc8-115">The **MDM\_Policy\_Config01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1edc8-116">Activehoursend</span><span class="sxs-lookup"><span data-stu-id="1edc8-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-119">Activehoursmaxrange</span><span class="sxs-lookup"><span data-stu-id="1edc8-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-122">Activehoursstart</span><span class="sxs-lookup"><span data-stu-id="1edc8-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-125">Allowautoupdate</span><span class="sxs-lookup"><span data-stu-id="1edc8-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-128">Allowautowindowsupdatedownloadovermeterednetwork</span><span class="sxs-lookup"><span data-stu-id="1edc8-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-131">Allowmuupdateservice</span><span class="sxs-lookup"><span data-stu-id="1edc8-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-134">Allownonmicrosoftsignetdupdate</span><span class="sxs-lookup"><span data-stu-id="1edc8-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="1edc8-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-140">Autorestartdeadlineperiodindays</span><span class="sxs-lookup"><span data-stu-id="1edc8-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-143">Autorestartnotificationschedule</span><span class="sxs-lookup"><span data-stu-id="1edc8-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-146">Autorestartrequirednotificationentlassung</span><span class="sxs-lookup"><span data-stu-id="1edc8-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="1edc8-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1edc8-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-155">Deferqualityupdatesperiodindays</span><span class="sxs-lookup"><span data-stu-id="1edc8-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="1edc8-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-161">Deferupgradezperiod</span><span class="sxs-lookup"><span data-stu-id="1edc8-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-164">Erkenctionfrequency</span><span class="sxs-lookup"><span data-stu-id="1edc8-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-167">Disabledualscan</span><span class="sxs-lookup"><span data-stu-id="1edc8-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-170">Engagedrestartstichtag</span><span class="sxs-lookup"><span data-stu-id="1edc8-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-173">Engagedrestartnoozeschedule</span><span class="sxs-lookup"><span data-stu-id="1edc8-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-174">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-176">Engagedrestarttransitionschedule</span><span class="sxs-lookup"><span data-stu-id="1edc8-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-177">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-179">Excluabwudriversinqualityupdate</span><span class="sxs-lookup"><span data-stu-id="1edc8-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-180">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-182">Fillemptycontenturls</span><span class="sxs-lookup"><span data-stu-id="1edc8-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-185">Ignoremoappdownloadlimit</span><span class="sxs-lookup"><span data-stu-id="1edc8-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-186">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-188">Ignoremoupdatedownloadlimit</span><span class="sxs-lookup"><span data-stu-id="1edc8-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1edc8-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1edc8-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1edc8-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1edc8-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-194">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1edc8-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1edc8-195">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="1edc8-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="1edc8-196">Für diese Klasse ist die Zeichenfolge "Update".</span><span class="sxs-lookup"><span data-stu-id="1edc8-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="1edc8-197">Managepreviewbuilds</span><span class="sxs-lookup"><span data-stu-id="1edc8-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-198">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1edc8-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1edc8-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1edc8-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1edc8-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-203">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1edc8-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1edc8-204">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="1edc8-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="1edc8-205">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="1edc8-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="1edc8-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="1edc8-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="1edc8-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-212">Pausefeatureupdatesstarttime</span><span class="sxs-lookup"><span data-stu-id="1edc8-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1edc8-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="1edc8-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-216">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-218">Pausequalityupdatesstarttime</span><span class="sxs-lookup"><span data-stu-id="1edc8-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1edc8-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-221">Phoneupdaterestrictions</span><span class="sxs-lookup"><span data-stu-id="1edc8-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-222">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="1edc8-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-225">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="1edc8-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-228">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="1edc8-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-231">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-233">Scheduledinstalleveryweek</span><span class="sxs-lookup"><span data-stu-id="1edc8-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-234">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-236">Scheduledinstallfirstweek</span><span class="sxs-lookup"><span data-stu-id="1edc8-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-237">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-239">Scheduledinstallfourthweek</span><span class="sxs-lookup"><span data-stu-id="1edc8-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-240">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-242">Scheduledinstallsecondweek</span><span class="sxs-lookup"><span data-stu-id="1edc8-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-243">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-245">Scheduledinstallthirdweek</span><span class="sxs-lookup"><span data-stu-id="1edc8-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-246">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="1edc8-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-249">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-251">Scheduleimminentrestartwarning</span><span class="sxs-lookup"><span data-stu-id="1edc8-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-252">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-254">Schedulerestartwarning</span><span class="sxs-lookup"><span data-stu-id="1edc8-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-255">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-257">Setautoriestartnotificationdeaktivieren</span><span class="sxs-lookup"><span data-stu-id="1edc8-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-258">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-260">"".</span><span class="sxs-lookup"><span data-stu-id="1edc8-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-261">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1edc8-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-263">Updateserviceurl</span><span class="sxs-lookup"><span data-stu-id="1edc8-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1edc8-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1edc8-266">Updateserviceurlalternate</span><span class="sxs-lookup"><span data-stu-id="1edc8-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edc8-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1edc8-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edc8-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1edc8-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1edc8-269">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1edc8-269">Requirements</span></span>



| <span data-ttu-id="1edc8-270">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1edc8-270">Requirement</span></span> | <span data-ttu-id="1edc8-271">Wert</span><span class="sxs-lookup"><span data-stu-id="1edc8-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1edc8-272">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1edc8-272">Minimum supported client</span></span><br/> | <span data-ttu-id="1edc8-273">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1edc8-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1edc8-274">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1edc8-274">Minimum supported server</span></span><br/> | <span data-ttu-id="1edc8-275">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1edc8-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1edc8-276">Namespace</span><span class="sxs-lookup"><span data-stu-id="1edc8-276">Namespace</span></span><br/>                | <span data-ttu-id="1edc8-277">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1edc8-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1edc8-278">MOF</span><span class="sxs-lookup"><span data-stu-id="1edc8-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1edc8-279"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1edc8-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1edc8-280">DLL</span><span class="sxs-lookup"><span data-stu-id="1edc8-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1edc8-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1edc8-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1edc8-282">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1edc8-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edc8-283">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="1edc8-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

