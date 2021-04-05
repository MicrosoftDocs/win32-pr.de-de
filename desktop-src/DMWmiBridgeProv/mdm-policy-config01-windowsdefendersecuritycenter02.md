---
title: MDM_Policy_Config01_WindowsDefenderSecurityCenter02-Klasse
description: Die Config01 WindowsDefenderSecurityCenter02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Windows Defender-Security Center Richtlinien dar.
ms.assetid: 406c3992-e9ed-49c5-a4c4-97d91013d416
keywords:
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02-Klasse
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b341eb66cc5d1186a962278babce536c0050523d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858929"
---
# <a name="mdm_policy_config01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="b00ee-105">MDM- \_ Richtlinie \_ Config01 \_ WindowsDefenderSecurityCenter02-Klasse</span><span class="sxs-lookup"><span data-stu-id="b00ee-105">MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="b00ee-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b00ee-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b00ee-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b00ee-108">Die Config01 WindowsDefenderSecurityCenter02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Windows Defender-Security Center Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="b00ee-108">The MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="b00ee-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b00ee-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00ee-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b00ee-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsDefenderSecurityCenter02
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

## <a name="members"></a><span data-ttu-id="b00ee-111">Member</span><span class="sxs-lookup"><span data-stu-id="b00ee-111">Members</span></span>

<span data-ttu-id="b00ee-112">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsDefenderSecurityCenter02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b00ee-112">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="b00ee-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b00ee-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b00ee-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b00ee-114">Properties</span></span>

<span data-ttu-id="b00ee-115">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsDefenderSecurityCenter02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b00ee-115">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b00ee-116">CompanyName</span><span class="sxs-lookup"><span data-stu-id="b00ee-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b00ee-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-119">Disableappbrowserui</span><span class="sxs-lookup"><span data-stu-id="b00ee-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-122">Disableenhancedbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b00ee-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-125">Disablefamilyui</span><span class="sxs-lookup"><span data-stu-id="b00ee-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-128">Disablehealthui</span><span class="sxs-lookup"><span data-stu-id="b00ee-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-131">Disablenetworkui</span><span class="sxs-lookup"><span data-stu-id="b00ee-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="b00ee-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-137">Disablevirusui</span><span class="sxs-lookup"><span data-stu-id="b00ee-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-140">Diszuweisung wexploitschutzoverride</span><span class="sxs-lookup"><span data-stu-id="b00ee-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-143">E-Mail</span><span class="sxs-lookup"><span data-stu-id="b00ee-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b00ee-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-146">Enablecustomizedtreasts</span><span class="sxs-lookup"><span data-stu-id="b00ee-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-149">Enableinappcustomianpassung</span><span class="sxs-lookup"><span data-stu-id="b00ee-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b00ee-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b00ee-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b00ee-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b00ee-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b00ee-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b00ee-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b00ee-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b00ee-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b00ee-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b00ee-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-159">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b00ee-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-160">Smartphone</span><span class="sxs-lookup"><span data-stu-id="b00ee-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b00ee-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b00ee-163">URL</span><span class="sxs-lookup"><span data-stu-id="b00ee-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b00ee-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b00ee-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b00ee-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b00ee-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b00ee-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b00ee-166">Requirements</span></span>



| <span data-ttu-id="b00ee-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b00ee-167">Requirement</span></span> | <span data-ttu-id="b00ee-168">Wert</span><span class="sxs-lookup"><span data-stu-id="b00ee-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b00ee-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b00ee-169">Minimum supported client</span></span><br/> | <span data-ttu-id="b00ee-170">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b00ee-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b00ee-171">Minimum supported server</span></span><br/> | <span data-ttu-id="b00ee-172">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b00ee-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b00ee-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="b00ee-173">Namespace</span></span><br/>                | <span data-ttu-id="b00ee-174">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b00ee-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b00ee-175">MOF</span><span class="sxs-lookup"><span data-stu-id="b00ee-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b00ee-176"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b00ee-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b00ee-177">DLL</span><span class="sxs-lookup"><span data-stu-id="b00ee-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b00ee-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b00ee-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

