---
title: MDM_Policy_Result01_Experience02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Experience02-Klasse stellt die verfügbaren Erfahrungs Richtlinien dar.
ms.assetid: c6dc2ef1-1f12-40b0-9d5f-9e886fe1e128
keywords:
- MDM_Policy_Result01_Experience02-Klasse
- MDM_Policy_Result01_Experience02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02.InstanceID
- MDM_Policy_Result01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a767c96d7ee23b4dad9719fa74850b39f0759b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040154"
---
# <a name="mdm_policy_result01_experience02-class"></a><span data-ttu-id="c43f3-105">MDM- \_ Richtlinie \_ Result01 \_ Experience02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c43f3-105">MDM\_Policy\_Result01\_Experience02 class</span></span>

<span data-ttu-id="c43f3-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c43f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c43f3-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c43f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c43f3-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Experience02** -Klasse stellt die verfügbaren Erfahrungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="c43f3-108">The **MDM\_Policy\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="c43f3-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c43f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43f3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c43f3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="c43f3-111">Member</span><span class="sxs-lookup"><span data-stu-id="c43f3-111">Members</span></span>

<span data-ttu-id="c43f3-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Experience02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c43f3-112">The **MDM\_Policy\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="c43f3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c43f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c43f3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c43f3-114">Properties</span></span>

<span data-ttu-id="c43f3-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Experience02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c43f3-115">The **MDM\_Policy\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c43f3-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="c43f3-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-119">Allowdevicediscovery</span><span class="sxs-lookup"><span data-stu-id="c43f3-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-122">Allowfindmydevice</span><span class="sxs-lookup"><span data-stu-id="c43f3-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-125">Allowmanualmdmuneinschreibung</span><span class="sxs-lookup"><span data-stu-id="c43f3-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-128">Allowsaveasofofficefiles</span><span class="sxs-lookup"><span data-stu-id="c43f3-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c43f3-131">Allowscreencapture</span><span class="sxs-lookup"><span data-stu-id="c43f3-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-134">Allowsharingofofficefiles</span><span class="sxs-lookup"><span data-stu-id="c43f3-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c43f3-137">Allowsimerrordialogprompt-nosim</span><span class="sxs-lookup"><span data-stu-id="c43f3-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="c43f3-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-143">Allowwindowstips</span><span class="sxs-lookup"><span data-stu-id="c43f3-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c43f3-146">Donotshowfeedbackbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c43f3-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c43f3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c43f3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c43f3-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c43f3-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c43f3-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c43f3-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c43f3-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c43f3-153">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="c43f3-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="c43f3-154">Für diese Klasse ist die Zeichenfolge "erleben".</span><span class="sxs-lookup"><span data-stu-id="c43f3-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="c43f3-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c43f3-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c43f3-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c43f3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c43f3-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c43f3-158">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c43f3-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c43f3-159">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="c43f3-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="c43f3-160">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="c43f3-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c43f3-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c43f3-161">Requirements</span></span>



| <span data-ttu-id="c43f3-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c43f3-162">Requirement</span></span> | <span data-ttu-id="c43f3-163">Wert</span><span class="sxs-lookup"><span data-stu-id="c43f3-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43f3-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c43f3-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c43f3-165">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c43f3-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c43f3-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c43f3-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c43f3-167">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c43f3-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c43f3-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="c43f3-168">Namespace</span></span><br/>                | <span data-ttu-id="c43f3-169">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c43f3-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c43f3-170">MOF</span><span class="sxs-lookup"><span data-stu-id="c43f3-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c43f3-171"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c43f3-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c43f3-172">DLL</span><span class="sxs-lookup"><span data-stu-id="c43f3-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c43f3-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c43f3-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c43f3-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c43f3-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43f3-175">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="c43f3-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

