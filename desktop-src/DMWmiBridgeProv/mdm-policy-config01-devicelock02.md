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
# <a name="mdm_policy_config01_devicelock02-class"></a>MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02** -Klasse stellt die verfügbaren Geräte Sperr Richtlinien dar.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceLock02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

Allowscreentimeoutwhilelockeduserconfig
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowsimpledebug Password](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Alpha anumericdebug-Element](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Geräte abgeleitete](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

DevicePasswordEnabled sollte nicht auf aktiviert (0) festgelegt werden, wenn WMI verwendet wird, um die EAS DeviceLock-Richtlinien festzulegen, da Sie standardmäßig in Richtlinien-CSP für die Back-Kompatibilität mit Windows 8. x aktiviert ist. Wenn die Einstellung für "deaktiviert" auf "aktiviert" (0) festgelegt ist, gibt der Richtlinien-CSP einen Fehler zurück, der besagt, dass "tvicepasswordenabled" bereits vorhanden ist. Windows 8. x hat die Richtlinie "devicepassword" nicht unterstützt. Beim Deaktivieren von DevicePasswordEnabled (1) sollte dies die einzige Richtlinie sein, die in der Gruppe "DeviceLock" der folgenden Richtlinien festgelegt ist. Die Richtlinien sind unten aufgeführt: >-"-Geräte abvicepasswordenabled" ist die übergeordnete Richtlinie der folgenden:

-   Die übergeordnete Richtlinie der folgenden ist:
    -   Allowsimpledebug Password
    -   MinDevicePasswordLength
    -   Alphanumerisch ist die übergeordnete Richtlinie von:
        -   MinDevicePasswordComplexCharacters 
    -   Maxde vicepasswordfailedattempts
    -   MaxInactivityTimeDeviceLock

</dd> <dt>

[DevicePasswordExpiration](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[DevicePasswordHistory](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Enforcelockscreenandlogonimage](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

Enforcelockscreenprovider
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "DeviceLock".

</dd> <dt>

[Maxde vicepasswordfailedattempts](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[MaxInactivityTimeDeviceLock](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[MinDevicePasswordComplexCharacters](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[MinDevicePasswordLength](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[MinimumPasswordAge](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".

</dd> <dt>

[Preventlockscreenslide Show](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

Screentimeoutwhilelocked
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

