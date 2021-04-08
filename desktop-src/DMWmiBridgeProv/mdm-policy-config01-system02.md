---
title: MDM_Policy_Config01_System02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ System02-Klasse stellt die verfügbaren System Richtlinien dar.
ms.assetid: 0C3E21DF-309C-4AF3-8682-E921BF45BDEF
keywords:
- MDM_Policy_ConfigSource01_System02-Klasse
- MDM_Policy_ConfigSource01_System02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02.InstanceID
- MDM_Policy_ConfigSource01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45ae8061b3e383abdd075d461d5b6dc2c46a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741673"
---
# <a name="mdm_policy_config01_system02-class"></a><span data-ttu-id="7e3c1-105">MDM- \_ Richtlinie \_ Config01 \_ System02-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e3c1-105">MDM\_Policy\_Config01\_System02 class</span></span>

<span data-ttu-id="7e3c1-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7e3c1-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7e3c1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7e3c1-108">Die **MDM- \_ Richtlinie \_ Config01 \_ System02** -Klasse stellt die verfügbaren System Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-108">The **MDM\_Policy\_Config01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="7e3c1-109">Diese Richtlinien bestimmen System Konfigurationen, die zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="7e3c1-110">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e3c1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e3c1-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_System02
{
  string InstanceID = "System";
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

## <a name="members"></a><span data-ttu-id="7e3c1-112">Member</span><span class="sxs-lookup"><span data-stu-id="7e3c1-112">Members</span></span>

<span data-ttu-id="7e3c1-113">Die **MDM- \_ Richtlinie \_ ConfigSource01 \_ System02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e3c1-113">The **MDM\_Policy\_ConfigSource01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="7e3c1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e3c1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e3c1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e3c1-115">Properties</span></span>

<span data-ttu-id="7e3c1-116">Die **MDM- \_ Richtlinie \_ ConfigSource01 \_ System02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-116">The **MDM\_Policy\_ConfigSource01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7e3c1-117">Allowbuildpreview</span><span class="sxs-lookup"><span data-stu-id="7e3c1-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-120">Zugwembeddedmode</span><span class="sxs-lookup"><span data-stu-id="7e3c1-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-123">Zuordnungs Datei</span><span class="sxs-lookup"><span data-stu-id="7e3c1-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-126">Allowfontproviders</span><span class="sxs-lookup"><span data-stu-id="7e3c1-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-127">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="7e3c1-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="7e3c1-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-133">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="7e3c1-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-136">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-138">"Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="7e3c1-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-139">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-141">Bootstartdriverinitialization</span><span class="sxs-lookup"><span data-stu-id="7e3c1-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="7e3c1-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-145">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-147">Disableonedrivefilesync</span><span class="sxs-lookup"><span data-stu-id="7e3c1-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-148">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-150">Disablesystemrestore</span><span class="sxs-lookup"><span data-stu-id="7e3c1-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e3c1-153">Feedbackhubalwayssavediagnosticslosch</span><span class="sxs-lookup"><span data-stu-id="7e3c1-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-154">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e3c1-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e3c1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-159">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e3c1-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e3c1-160">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="7e3c1-161">Für diese Klasse ist die Zeichenfolge "System".</span><span class="sxs-lookup"><span data-stu-id="7e3c1-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="7e3c1-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e3c1-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-163">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e3c1-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e3c1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-168">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e3c1-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e3c1-169">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="7e3c1-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="7e3c1-170">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="7e3c1-170">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

<span data-ttu-id="7e3c1-171">"./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="7e3c1-171">"./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="7e3c1-172">Telemetryproxy</span><span class="sxs-lookup"><span data-stu-id="7e3c1-172">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3c1-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e3c1-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e3c1-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e3c1-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e3c1-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e3c1-175">Requirements</span></span>



| <span data-ttu-id="7e3c1-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e3c1-176">Requirement</span></span> | <span data-ttu-id="7e3c1-177">Wert</span><span class="sxs-lookup"><span data-stu-id="7e3c1-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e3c1-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e3c1-178">Minimum supported client</span></span><br/> | <span data-ttu-id="7e3c1-179">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e3c1-179">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e3c1-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e3c1-180">Minimum supported server</span></span><br/> | <span data-ttu-id="7e3c1-181">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7e3c1-181">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7e3c1-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e3c1-182">Namespace</span></span><br/>                | <span data-ttu-id="7e3c1-183">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7e3c1-183">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7e3c1-184">MOF</span><span class="sxs-lookup"><span data-stu-id="7e3c1-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e3c1-185"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e3c1-185"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e3c1-186">DLL</span><span class="sxs-lookup"><span data-stu-id="7e3c1-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e3c1-187"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e3c1-187"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e3c1-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e3c1-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e3c1-189">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="7e3c1-189">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

