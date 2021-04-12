---
title: MDM_Policy_Result01_WindowsDefenderSecurityCenter02-Klasse
description: Die Result01 WindowsDefenderSecurityCenter02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Windows Defender-Security Center Richtlinien dar.
ms.assetid: 59047e16-a188-4ec9-9d1b-db2b15c1109b
keywords:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02-Klasse
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7739410347169637ca5f27fef5627e26f8347c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475312"
---
# <a name="mdm_policy_result01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="bc37c-105">MDM- \_ Richtlinie \_ Result01 \_ WindowsDefenderSecurityCenter02-Klasse</span><span class="sxs-lookup"><span data-stu-id="bc37c-105">MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="bc37c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="bc37c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc37c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="bc37c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc37c-108">Die Result01 WindowsDefenderSecurityCenter02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Windows Defender-Security Center Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="bc37c-108">The MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="bc37c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bc37c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc37c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc37c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="bc37c-111">Member</span><span class="sxs-lookup"><span data-stu-id="bc37c-111">Members</span></span>

<span data-ttu-id="bc37c-112">Die **MDM- \_ Richtlinie \_ Result01 \_ WindowsDefenderSecurityCenter02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bc37c-112">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc37c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc37c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc37c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc37c-114">Properties</span></span>

<span data-ttu-id="bc37c-115">Die **MDM- \_ Richtlinie \_ Result01 \_ WindowsDefenderSecurityCenter02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc37c-115">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bc37c-116">CompanyName</span><span class="sxs-lookup"><span data-stu-id="bc37c-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc37c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-119">Disableappbrowserui</span><span class="sxs-lookup"><span data-stu-id="bc37c-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-122">Disableenhancedbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bc37c-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-125">Disablefamilyui</span><span class="sxs-lookup"><span data-stu-id="bc37c-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-128">Disablehealthui</span><span class="sxs-lookup"><span data-stu-id="bc37c-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-131">Disablenetworkui</span><span class="sxs-lookup"><span data-stu-id="bc37c-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="bc37c-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-137">Disablevirusui</span><span class="sxs-lookup"><span data-stu-id="bc37c-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-140">Diszuweisung wexploitschutzoverride</span><span class="sxs-lookup"><span data-stu-id="bc37c-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-143">E-Mail</span><span class="sxs-lookup"><span data-stu-id="bc37c-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc37c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-146">Enablecustomizedtreasts</span><span class="sxs-lookup"><span data-stu-id="bc37c-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-149">Enableinappcustomianpassung</span><span class="sxs-lookup"><span data-stu-id="bc37c-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc37c-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc37c-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc37c-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc37c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bc37c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc37c-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc37c-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bc37c-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc37c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bc37c-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-159">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc37c-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-160">Smartphone</span><span class="sxs-lookup"><span data-stu-id="bc37c-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc37c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc37c-163">URL</span><span class="sxs-lookup"><span data-stu-id="bc37c-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc37c-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc37c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc37c-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc37c-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc37c-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc37c-166">Requirements</span></span>



| <span data-ttu-id="bc37c-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc37c-167">Requirement</span></span> | <span data-ttu-id="bc37c-168">Wert</span><span class="sxs-lookup"><span data-stu-id="bc37c-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc37c-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc37c-169">Minimum supported client</span></span><br/> | <span data-ttu-id="bc37c-170">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc37c-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc37c-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc37c-171">Minimum supported server</span></span><br/> | <span data-ttu-id="bc37c-172">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc37c-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc37c-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc37c-173">Namespace</span></span><br/>                | <span data-ttu-id="bc37c-174">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bc37c-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bc37c-175">MOF</span><span class="sxs-lookup"><span data-stu-id="bc37c-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc37c-176"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc37c-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc37c-177">DLL</span><span class="sxs-lookup"><span data-stu-id="bc37c-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc37c-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc37c-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

