---
title: MDM_Policy_Config01_Defender02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Defender02class stellt Richtlinien für Windows Defender dar.
ms.assetid: 6d9d4edd-fcb6-45ea-bc5d-1bffb9cf8740
keywords:
- MDM_Policy_Config01_Defender02-Klasse
- MDM_Policy_Config01_Defender02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02.InstanceID
- MDM_Policy_Config01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b184008fc0ce7fc44dcb7106ceec3abc0e91450d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476017"
---
# <a name="mdm_policy_config01_defender02-class"></a><span data-ttu-id="93ebf-105">MDM- \_ Richtlinie \_ Config01 \_ Defender02-Klasse</span><span class="sxs-lookup"><span data-stu-id="93ebf-105">MDM\_Policy\_Config01\_Defender02 class</span></span>

<span data-ttu-id="93ebf-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="93ebf-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="93ebf-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="93ebf-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="93ebf-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Defender02**-Klasse stellt Richtlinien für Windows Defender dar.</span><span class="sxs-lookup"><span data-stu-id="93ebf-108">The **MDM\_Policy\_Config01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="93ebf-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93ebf-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ebf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="93ebf-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Defender02
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
  sint32 ScanParameter;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
};
```

## <a name="members"></a><span data-ttu-id="93ebf-111">Member</span><span class="sxs-lookup"><span data-stu-id="93ebf-111">Members</span></span>

<span data-ttu-id="93ebf-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Defender02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="93ebf-112">The **MDM\_Policy\_Config01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="93ebf-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93ebf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93ebf-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93ebf-114">Properties</span></span>

<span data-ttu-id="93ebf-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Defender02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93ebf-115">The **MDM\_Policy\_Config01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="93ebf-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="93ebf-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="93ebf-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="93ebf-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="93ebf-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="93ebf-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="93ebf-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="93ebf-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="93ebf-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="93ebf-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="93ebf-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="93ebf-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="93ebf-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="93ebf-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-155">Angreigeereductiononlyausschlüsse</span><span class="sxs-lookup"><span data-stu-id="93ebf-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-158">Angreiderereductionrules</span><span class="sxs-lookup"><span data-stu-id="93ebf-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="93ebf-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-164">Cloudblocklevel</span><span class="sxs-lookup"><span data-stu-id="93ebf-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-167">Cloudextendedtimeout</span><span class="sxs-lookup"><span data-stu-id="93ebf-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-170">Controlledfolderaccesszuwebdapplications</span><span class="sxs-lookup"><span data-stu-id="93ebf-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-173">Controlledfolderaccessprotectedfolders</span><span class="sxs-lookup"><span data-stu-id="93ebf-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="93ebf-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-177">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-179">Enablecontrolledfolderaccess</span><span class="sxs-lookup"><span data-stu-id="93ebf-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-180">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-182">Enablenetworkprotection</span><span class="sxs-lookup"><span data-stu-id="93ebf-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="93ebf-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="93ebf-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="93ebf-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93ebf-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93ebf-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93ebf-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-197">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="93ebf-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="93ebf-198">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="93ebf-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="93ebf-199">Für diese Klasse ist die Zeichenfolge "Defender".</span><span class="sxs-lookup"><span data-stu-id="93ebf-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="93ebf-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="93ebf-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93ebf-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-203">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="93ebf-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="93ebf-204">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="93ebf-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="93ebf-205">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="93ebf-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="93ebf-206">Puaprotection</span><span class="sxs-lookup"><span data-stu-id="93ebf-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="93ebf-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="93ebf-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-213">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="93ebf-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-216">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="93ebf-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="93ebf-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-222">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="93ebf-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-225">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="93ebf-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-228">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93ebf-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="93ebf-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="93ebf-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ebf-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93ebf-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ebf-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="93ebf-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93ebf-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93ebf-233">Requirements</span></span>



| <span data-ttu-id="93ebf-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93ebf-234">Requirement</span></span> | <span data-ttu-id="93ebf-235">Wert</span><span class="sxs-lookup"><span data-stu-id="93ebf-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ebf-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93ebf-236">Minimum supported client</span></span><br/> | <span data-ttu-id="93ebf-237">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93ebf-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93ebf-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93ebf-238">Minimum supported server</span></span><br/> | <span data-ttu-id="93ebf-239">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="93ebf-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="93ebf-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="93ebf-240">Namespace</span></span><br/>                | <span data-ttu-id="93ebf-241">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="93ebf-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="93ebf-242">MOF</span><span class="sxs-lookup"><span data-stu-id="93ebf-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93ebf-243"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="93ebf-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="93ebf-244">DLL</span><span class="sxs-lookup"><span data-stu-id="93ebf-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ebf-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ebf-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ebf-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93ebf-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ebf-247">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="93ebf-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

