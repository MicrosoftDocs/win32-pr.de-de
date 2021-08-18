---
description: Stellt den konfigurierten Zustand der Sicherheitseinstellungen für dar.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22bc30db51b103f50eaa4deed7ca6f479c5f94600fbb15ef2a6f4bb36595d159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148144"
---
# <a name="msvm_securitysettingdata-class"></a>Msvm \_ SecuritySettingData-Klasse

Stellt den konfigurierten Zustand der Sicherheitseinstellungen für einen virtuellen Computer dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SecuritySettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SecuritySettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**TRUE zum** Anfordern des Datenschutzes für einen virtuellen Computer; andernfalls **FALSE.** Der Standardwert ist **false.**

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**TRUE,** damit der Zustands- und Migrationsdatenverkehr eines virtuellen Computers verschlüsselt ist; andernfalls **FALSE.** Der Standardwert für einen neu erstellten virtuellen Computer ist **false.**

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**TRUE,** um ein Schlüsselspeichergerät (Key Storage Device, KSD) für diesen virtuellen Computer zu aktivieren; andernfalls **FALSE.** Ein neu erstellter virtueller Computer verfügt über eine deaktivierte KSD.

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**"true"** zum Anfordern der Abschirmung für einen virtuellen Computer; andernfalls **FALSE.** Ein neu erstellter virtueller Computer hat den anfänglichen angeforderten Schutzstatus **false.**

</dd> <dt>

**TpmEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**TRUE,** um ein Trusted Platform Nodule (TPM) für diesen virtuellen Computer zu aktivieren; andernfalls **FALSE.** Ein neu erstellter virtueller Computer verfügt über ein deaktiviertes TPM.

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**"true",** wenn keine virtualisierungsbasierte Sicherheit für virtuelle Computer angeboten wird; andernfalls **FALSE.** Die Standardeinstellung für den Abmeldestatus eines neu erstellten virtuellen Computers ist **false.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

