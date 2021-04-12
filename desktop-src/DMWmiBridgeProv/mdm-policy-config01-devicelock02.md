---
title: MDM_Policy_Config01_DeviceLock02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02-Klasse stellt die verfügbaren Geräte Sperr Richtlinien dar.
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- MDM_Policy_Config01_DeviceLock02-Klasse
- MDM_Policy_Config01_DeviceLock02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105728"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="211dd-105">MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02-Klasse</span><span class="sxs-lookup"><span data-stu-id="211dd-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="211dd-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="211dd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="211dd-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="211dd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="211dd-108">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02** -Klasse stellt die verfügbaren Geräte Sperr Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="211dd-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="211dd-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="211dd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="211dd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="211dd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="211dd-111">Member</span><span class="sxs-lookup"><span data-stu-id="211dd-111">Members</span></span>

<span data-ttu-id="211dd-112">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="211dd-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="211dd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="211dd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="211dd-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="211dd-114">Properties</span></span>

<span data-ttu-id="211dd-115">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="211dd-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="211dd-116">Allowscreentimeoutwhilelockeduserconfig</span><span class="sxs-lookup"><span data-stu-id="211dd-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-119">Allowsimpledebug Password</span><span class="sxs-lookup"><span data-stu-id="211dd-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-122">Alpha anumericdebug-Element</span><span class="sxs-lookup"><span data-stu-id="211dd-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-125">Geräte abgeleitete</span><span class="sxs-lookup"><span data-stu-id="211dd-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="211dd-128">DevicePasswordEnabled sollte nicht auf aktiviert (0) festgelegt werden, wenn WMI verwendet wird, um die EAS DeviceLock-Richtlinien festzulegen, da Sie standardmäßig in Richtlinien-CSP für die Back-Kompatibilität mit Windows 8. x aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="211dd-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="211dd-129">Wenn die Einstellung für "deaktiviert" auf "aktiviert" (0) festgelegt ist, gibt der Richtlinien-CSP einen Fehler zurück, der besagt, dass "tvicepasswordenabled" bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="211dd-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="211dd-130">Windows 8. x hat die Richtlinie "devicepassword" nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="211dd-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="211dd-131">Beim Deaktivieren von DevicePasswordEnabled (1) sollte dies die einzige Richtlinie sein, die in der Gruppe "DeviceLock" der folgenden Richtlinien festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="211dd-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="211dd-132">Die Richtlinien sind unten aufgeführt: >-"-Geräte abvicepasswordenabled" ist die übergeordnete Richtlinie der folgenden:</span><span class="sxs-lookup"><span data-stu-id="211dd-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="211dd-133">Die übergeordnete Richtlinie der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="211dd-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="211dd-134">Allowsimpledebug Password</span><span class="sxs-lookup"><span data-stu-id="211dd-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="211dd-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="211dd-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="211dd-136">Alphanumerisch ist die übergeordnete Richtlinie von:</span><span class="sxs-lookup"><span data-stu-id="211dd-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="211dd-137">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="211dd-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="211dd-138">Maxde vicepasswordfailedattempts</span><span class="sxs-lookup"><span data-stu-id="211dd-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="211dd-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="211dd-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="211dd-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="211dd-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="211dd-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-146">Enforcelockscreenandlogonimage</span><span class="sxs-lookup"><span data-stu-id="211dd-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211dd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="211dd-149">Enforcelockscreenprovider</span><span class="sxs-lookup"><span data-stu-id="211dd-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211dd-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="211dd-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="211dd-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211dd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="211dd-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211dd-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="211dd-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="211dd-156">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="211dd-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="211dd-157">Für diese Klasse ist die Zeichenfolge "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="211dd-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="211dd-158">Maxde vicepasswordfailedattempts</span><span class="sxs-lookup"><span data-stu-id="211dd-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="211dd-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-164">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="211dd-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="211dd-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="211dd-170">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="211dd-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="211dd-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="211dd-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211dd-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="211dd-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211dd-176">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="211dd-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="211dd-177">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="211dd-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="211dd-178">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="211dd-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="211dd-179">Preventlockscreenslide Show</span><span class="sxs-lookup"><span data-stu-id="211dd-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211dd-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="211dd-182">Screentimeoutwhilelocked</span><span class="sxs-lookup"><span data-stu-id="211dd-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211dd-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="211dd-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="211dd-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211dd-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="211dd-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="211dd-185">Requirements</span></span>



| <span data-ttu-id="211dd-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="211dd-186">Requirement</span></span> | <span data-ttu-id="211dd-187">Wert</span><span class="sxs-lookup"><span data-stu-id="211dd-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="211dd-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="211dd-188">Minimum supported client</span></span><br/> | <span data-ttu-id="211dd-189">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="211dd-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="211dd-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="211dd-190">Minimum supported server</span></span><br/> | <span data-ttu-id="211dd-191">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="211dd-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="211dd-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="211dd-192">Namespace</span></span><br/>                | <span data-ttu-id="211dd-193">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="211dd-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="211dd-194">MOF</span><span class="sxs-lookup"><span data-stu-id="211dd-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="211dd-195"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="211dd-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="211dd-196">DLL</span><span class="sxs-lookup"><span data-stu-id="211dd-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211dd-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="211dd-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="211dd-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="211dd-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211dd-199">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="211dd-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

