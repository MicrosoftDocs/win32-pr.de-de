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
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347396"
---
# <a name="msvm_securitysettingdata-class"></a>MSVM \_ securitysettingdata-Klasse

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

Die **MSVM \_ securitysettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ securitysettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Dataschutzanforderung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

" **true** ", um den Schutz von Daten für eine VM anzufordern. andernfalls **false**. Der Standardwert ist **false.**

</dd> <dt>

**Verschlüsselungsstateandvmmigrationtraffic**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** , wenn der Zustands-und Migrations Datenverkehr einer verschlüsselten VM verschlüsselt werden soll. andernfalls **false**. Der Standardwert für eine neu erstellte VM ist **false**.

</dd> <dt>

**Ksdenabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

" **true** ", um ein Schlüsselspeicher Gerät (KSD) für diesen virtuellen Computer zu aktivieren. andernfalls **false**. Eine neu erstellte VM verfügt über eine deaktivierte KSD.

</dd> <dt>

**Shieldingrequessiert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

" **true** ", um den Schutz für eine VM anzufordern. andernfalls **false**. Ein neu erstellter virtueller Computer verfügt über einen anfänglichen Schutz angeforderten Status **false**.

</dd> <dt>

**Tpmenabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

" **true** ", um ein vertrauenswürdiges Plattform-nodule (TPM) für diesen virtuellen Computer zu aktivieren. andernfalls **false**. Ein neu erstellter virtueller Computer verfügt über ein TPM deaktivieren.

</dd> <dt>

**Virtualizationbasedsecurityoptout**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

" **true** ", wenn keine VM-virtualisierungsbasierte Sicherheit angeboten werden soll. andernfalls **false**. Die Standardeinstellung für einen neu erstellten VM-Abmelde Status ist **false**.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

