---
title: MDM_Policy_Result01_System02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ System02-Klasse stellt die verfügbaren System Richtlinien dar.
ms.assetid: 9A0D9688-9062-429F-897F-75705DC8FD79
keywords:
- MDM_Policy_Result01_System02-Klasse
- MDM_Policy_Result01_System02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02.InstanceID
- MDM_Policy_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffedc3c4e0eda857c071a3174690ad9677fd97da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741193"
---
# <a name="mdm_policy_result01_system02-class"></a><span data-ttu-id="ecb11-105">MDM- \_ Richtlinie \_ Result01 \_ System02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ecb11-105">MDM\_Policy\_Result01\_System02 class</span></span>

<span data-ttu-id="ecb11-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ecb11-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ecb11-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ecb11-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ecb11-108">Die **MDM- \_ Richtlinie \_ Result01 \_ System02** -Klasse stellt die verfügbaren System Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="ecb11-108">The **MDM\_Policy\_Result01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="ecb11-109">Diese Richtlinien bestimmen System Konfigurationen, die zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ecb11-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="ecb11-110">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ecb11-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb11-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecb11-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="ecb11-112">Member</span><span class="sxs-lookup"><span data-stu-id="ecb11-112">Members</span></span>

<span data-ttu-id="ecb11-113">Die **MDM- \_ Richtlinie \_ Result01 \_ System02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ecb11-113">The **MDM\_Policy\_Result01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="ecb11-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecb11-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecb11-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecb11-115">Properties</span></span>

<span data-ttu-id="ecb11-116">Die **MDM- \_ Richtlinie \_ Result01 \_ System02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ecb11-116">The **MDM\_Policy\_Result01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ecb11-117">Allowbuildpreview</span><span class="sxs-lookup"><span data-stu-id="ecb11-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-120">Zugwembeddedmode</span><span class="sxs-lookup"><span data-stu-id="ecb11-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-123">Zuordnungs Datei</span><span class="sxs-lookup"><span data-stu-id="ecb11-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-126">Allowfontproviders</span><span class="sxs-lookup"><span data-stu-id="ecb11-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-127">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="ecb11-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="ecb11-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-133">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="ecb11-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-136">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-138">"Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="ecb11-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-139">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-141">Bootstartdriverinitialization</span><span class="sxs-lookup"><span data-stu-id="ecb11-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ecb11-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="ecb11-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-145">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-147">Disableonedrivefilesync</span><span class="sxs-lookup"><span data-stu-id="ecb11-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-148">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-150">Disablesystemrestore</span><span class="sxs-lookup"><span data-stu-id="ecb11-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ecb11-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecb11-153">Feedbackhubalwayssavediagnosticslosch</span><span class="sxs-lookup"><span data-stu-id="ecb11-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-154">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecb11-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ecb11-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ecb11-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecb11-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-159">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecb11-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecb11-160">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ecb11-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="ecb11-161">Für diese Klasse ist die Zeichenfolge "System".</span><span class="sxs-lookup"><span data-stu-id="ecb11-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="ecb11-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="ecb11-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-163">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecb11-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecb11-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ecb11-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ecb11-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecb11-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-168">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecb11-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecb11-169">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ecb11-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="ecb11-170">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="ecb11-170">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="ecb11-171">Telemetryproxy</span><span class="sxs-lookup"><span data-stu-id="ecb11-171">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb11-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ecb11-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb11-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ecb11-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecb11-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecb11-174">Requirements</span></span>



| <span data-ttu-id="ecb11-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecb11-175">Requirement</span></span> | <span data-ttu-id="ecb11-176">Wert</span><span class="sxs-lookup"><span data-stu-id="ecb11-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb11-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecb11-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb11-178">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecb11-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ecb11-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecb11-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb11-180">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ecb11-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ecb11-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="ecb11-181">Namespace</span></span><br/>                | <span data-ttu-id="ecb11-182">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ecb11-182">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ecb11-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ecb11-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecb11-184"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ecb11-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecb11-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb11-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb11-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb11-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb11-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecb11-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb11-188">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ecb11-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

