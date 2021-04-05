---
title: MDM_Policy_Result01_DeviceLock02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ DeviceLock02-Klasse stellt die verfügbaren Geräte Sperr Richtlinien dar.
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- MDM_Policy_Result01_DeviceLock02-Klasse
- MDM_Policy_Result01_DeviceLock02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858925"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="12645-105">MDM- \_ Richtlinie \_ Result01 \_ DeviceLock02-Klasse</span><span class="sxs-lookup"><span data-stu-id="12645-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="12645-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="12645-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="12645-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="12645-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="12645-108">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceLock02** -Klasse stellt die verfügbaren Geräte Sperr Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="12645-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="12645-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="12645-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12645-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="12645-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="12645-111">Member</span><span class="sxs-lookup"><span data-stu-id="12645-111">Members</span></span>

<span data-ttu-id="12645-112">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceLock02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="12645-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="12645-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12645-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12645-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12645-114">Properties</span></span>

<span data-ttu-id="12645-115">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceLock02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12645-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12645-116">Allowscreentimeoutwhilelockeduserconfig</span><span class="sxs-lookup"><span data-stu-id="12645-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-119">Allowsimpledebug Password</span><span class="sxs-lookup"><span data-stu-id="12645-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-122">Alpha anumericdebug-Element</span><span class="sxs-lookup"><span data-stu-id="12645-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-125">Geräte abgeleitete</span><span class="sxs-lookup"><span data-stu-id="12645-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="12645-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="12645-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-134">Enforcelockscreenandlogonimage</span><span class="sxs-lookup"><span data-stu-id="12645-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12645-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12645-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="12645-137">Enforcelockscreenprovider</span><span class="sxs-lookup"><span data-stu-id="12645-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12645-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12645-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="12645-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="12645-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12645-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12645-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12645-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12645-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="12645-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="12645-144">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="12645-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="12645-145">Für diese Klasse ist die Zeichenfolge "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="12645-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="12645-146">Maxde vicepasswordfailedattempts</span><span class="sxs-lookup"><span data-stu-id="12645-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="12645-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-152">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="12645-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="12645-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12645-158">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="12645-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="12645-161">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="12645-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12645-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12645-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12645-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12645-164">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="12645-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="12645-165">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="12645-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="12645-166">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="12645-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="12645-167">Preventlockscreenslide Show</span><span class="sxs-lookup"><span data-stu-id="12645-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12645-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12645-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="12645-170">Screentimeoutwhilelocked</span><span class="sxs-lookup"><span data-stu-id="12645-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12645-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12645-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="12645-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12645-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12645-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12645-173">Requirements</span></span>



| <span data-ttu-id="12645-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12645-174">Requirement</span></span> | <span data-ttu-id="12645-175">Wert</span><span class="sxs-lookup"><span data-stu-id="12645-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12645-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12645-176">Minimum supported client</span></span><br/> | <span data-ttu-id="12645-177">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12645-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12645-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12645-178">Minimum supported server</span></span><br/> | <span data-ttu-id="12645-179">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="12645-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="12645-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="12645-180">Namespace</span></span><br/>                | <span data-ttu-id="12645-181">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="12645-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="12645-182">MOF</span><span class="sxs-lookup"><span data-stu-id="12645-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12645-183"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="12645-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="12645-184">DLL</span><span class="sxs-lookup"><span data-stu-id="12645-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12645-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12645-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12645-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12645-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12645-187">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="12645-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

