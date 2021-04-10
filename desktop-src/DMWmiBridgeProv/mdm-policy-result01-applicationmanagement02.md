---
title: MDM_Policy_Result01_ApplicationManagement02-Klasse
description: Die MDM \_ Policy \_ Result01 \_ ApplicationManagement02-Klasse stellt die verfügbaren Richtlinien zur Anwendungs Verwaltung dar. MDM \_ Policy \_ Result01 \_ ApplicationManagement02-Klasse stellt die verfügbaren Richtlinien zur Anwendungs Verwaltung dar.
ms.assetid: 141614e4-b2b1-49d9-879c-f6f86bee070c
keywords:
- MDM_Policy_Result01_ApplicationManagement02-Klasse
- MDM_Policy_Result01_ApplicationManagement02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationManagement02
- MDM_Policy_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477e4e58216c912aa14ec17b8e5879643e3de83f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103880"
---
# <a name="mdm_policy_result01_applicationmanagement02-class"></a><span data-ttu-id="11e0e-105">MDM- \_ Richtlinie \_ Result01 \_ ApplicationManagement02-Klasse</span><span class="sxs-lookup"><span data-stu-id="11e0e-105">MDM\_Policy\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="11e0e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="11e0e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11e0e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="11e0e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11e0e-108">Die **MDM \_ Policy \_ Result01 \_ ApplicationManagement02** -Klasse stellt die verfügbaren Richtlinien zur Anwendungs Verwaltung dar.</span><span class="sxs-lookup"><span data-stu-id="11e0e-108">The **MDM\_Policy\_Result01\_ApplicationManagement02** class represents the application management policies available.</span></span>

<span data-ttu-id="11e0e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="11e0e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e0e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="11e0e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a><span data-ttu-id="11e0e-111">Member</span><span class="sxs-lookup"><span data-stu-id="11e0e-111">Members</span></span>

<span data-ttu-id="11e0e-112">Die **MDM- \_ Richtlinie \_ Result01 \_ ApplicationManagement02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11e0e-112">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="11e0e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11e0e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11e0e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11e0e-114">Properties</span></span>

<span data-ttu-id="11e0e-115">Die **MDM- \_ Richtlinie \_ Result01 \_ ApplicationManagement02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11e0e-115">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="11e0e-116">AllowAllTrustedApps</span><span class="sxs-lookup"><span data-stu-id="11e0e-116">AllowAllTrustedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11e0e-119">Allowappstoreautoupdate</span><span class="sxs-lookup"><span data-stu-id="11e0e-119">AllowAppStoreAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11e0e-122">Allowdeveloperunlock</span><span class="sxs-lookup"><span data-stu-id="11e0e-122">AllowDeveloperUnlock</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11e0e-125">Allowgamedvr</span><span class="sxs-lookup"><span data-stu-id="11e0e-125">AllowGameDVR</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11e0e-128">Allowshareduserappdata</span><span class="sxs-lookup"><span data-stu-id="11e0e-128">AllowSharedUserAppData</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11e0e-131">Disablestoreoriginatedapps</span><span class="sxs-lookup"><span data-stu-id="11e0e-131">DisableStoreOriginatedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11e0e-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11e0e-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11e0e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11e0e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11e0e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11e0e-138">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="11e0e-138">Identifies the name of the parent node.</span></span> <span data-ttu-id="11e0e-139">Für diese Klasse ist die Zeichenfolge "ApplicationManagement".</span><span class="sxs-lookup"><span data-stu-id="11e0e-139">For this class, the string is "ApplicationManagement".</span></span>

</dd> <dt>

<span data-ttu-id="11e0e-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="11e0e-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11e0e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11e0e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11e0e-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11e0e-144">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="11e0e-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="11e0e-145">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="11e0e-145">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="11e0e-146">Restrictappdatatosystemvolume</span><span class="sxs-lookup"><span data-stu-id="11e0e-146">RestrictAppDataToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11e0e-149">Restrictappdesystemvolume</span><span class="sxs-lookup"><span data-stu-id="11e0e-149">RestrictAppToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e0e-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e0e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e0e-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11e0e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11e0e-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11e0e-152">Requirements</span></span>



| <span data-ttu-id="11e0e-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11e0e-153">Requirement</span></span> | <span data-ttu-id="11e0e-154">Wert</span><span class="sxs-lookup"><span data-stu-id="11e0e-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e0e-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11e0e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="11e0e-156">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11e0e-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11e0e-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11e0e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="11e0e-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11e0e-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11e0e-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="11e0e-159">Namespace</span></span><br/>                | <span data-ttu-id="11e0e-160">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="11e0e-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="11e0e-161">MOF</span><span class="sxs-lookup"><span data-stu-id="11e0e-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11e0e-162"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="11e0e-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11e0e-163">DLL</span><span class="sxs-lookup"><span data-stu-id="11e0e-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e0e-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e0e-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e0e-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11e0e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e0e-166">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="11e0e-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

