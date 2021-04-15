---
title: MDM_Policy_Result01_Defender02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Defender02class stellt Richtlinien für Windows Defender dar.
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- MDM_Policy_Result01_Defender02-Klasse
- MDM_Policy_Result01_Defender02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475891"
---
# <a name="mdm_policy_result01_defender02-class"></a><span data-ttu-id="9ba98-105">MDM- \_ Richtlinie \_ Result01 \_ Defender02-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ba98-105">MDM\_Policy\_Result01\_Defender02 class</span></span>

<span data-ttu-id="9ba98-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9ba98-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9ba98-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="9ba98-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9ba98-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Defender02**-Klasse stellt Richtlinien für Windows Defender dar.</span><span class="sxs-lookup"><span data-stu-id="9ba98-108">The **MDM\_Policy\_Result01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="9ba98-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ba98-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba98-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ba98-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a><span data-ttu-id="9ba98-111">Member</span><span class="sxs-lookup"><span data-stu-id="9ba98-111">Members</span></span>

<span data-ttu-id="9ba98-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Defender02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9ba98-112">The **MDM\_Policy\_Result01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="9ba98-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ba98-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ba98-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ba98-114">Properties</span></span>

<span data-ttu-id="9ba98-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Defender02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ba98-115">The **MDM\_Policy\_Result01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9ba98-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="9ba98-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="9ba98-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="9ba98-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="9ba98-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="9ba98-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="9ba98-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="9ba98-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="9ba98-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="9ba98-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="9ba98-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="9ba98-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="9ba98-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="9ba98-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-155">Angreigeereductiononlyausschlüsse</span><span class="sxs-lookup"><span data-stu-id="9ba98-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-158">Angreiderereductionrules</span><span class="sxs-lookup"><span data-stu-id="9ba98-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="9ba98-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-164">Cloudblocklevel</span><span class="sxs-lookup"><span data-stu-id="9ba98-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-167">Cloudextendedtimeout</span><span class="sxs-lookup"><span data-stu-id="9ba98-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-170">Controlledfolderaccesszuwebdapplications</span><span class="sxs-lookup"><span data-stu-id="9ba98-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-173">Controlledfolderaccessprotectedfolders</span><span class="sxs-lookup"><span data-stu-id="9ba98-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="9ba98-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-177">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-179">Enablecontrolledfolderaccess</span><span class="sxs-lookup"><span data-stu-id="9ba98-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-180">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-182">Enablenetworkprotection</span><span class="sxs-lookup"><span data-stu-id="9ba98-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="9ba98-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="9ba98-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="9ba98-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9ba98-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9ba98-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba98-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-197">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ba98-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ba98-198">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="9ba98-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="9ba98-199">Für diese Klasse ist die Zeichenfolge "Defender".</span><span class="sxs-lookup"><span data-stu-id="9ba98-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="9ba98-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9ba98-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba98-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-203">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ba98-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ba98-204">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="9ba98-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="9ba98-205">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="9ba98-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="9ba98-206">Puaprotection</span><span class="sxs-lookup"><span data-stu-id="9ba98-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="9ba98-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="9ba98-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-213">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="9ba98-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-216">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="9ba98-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="9ba98-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-222">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="9ba98-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-225">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="9ba98-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-228">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9ba98-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ba98-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="9ba98-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba98-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ba98-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba98-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ba98-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ba98-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ba98-233">Requirements</span></span>



| <span data-ttu-id="9ba98-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba98-234">Requirement</span></span> | <span data-ttu-id="9ba98-235">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba98-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba98-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ba98-236">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba98-237">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba98-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ba98-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ba98-238">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba98-239">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ba98-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9ba98-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ba98-240">Namespace</span></span><br/>                | <span data-ttu-id="9ba98-241">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9ba98-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9ba98-242">MOF</span><span class="sxs-lookup"><span data-stu-id="9ba98-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ba98-243"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9ba98-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ba98-244">DLL</span><span class="sxs-lookup"><span data-stu-id="9ba98-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ba98-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ba98-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba98-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ba98-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba98-247">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="9ba98-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

