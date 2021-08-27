---
description: Ordnet einen virtuellen Computer und seine Geräte Instanzen von CIM SettingData zu, die die aktuellen Einstellungen \_ darstellen, die für diese Objekte gelten.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eea8a6cce263ddb3ad00ecd6951c1d5b47c6d98d58e99763b3f28780cb3438b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950464"
---
# <a name="msvm_settingsdefinestate-class"></a>Msvm \_ SettingsDefineState-Klasse

Ordnet einen virtuellen Computer und seine Geräte Instanzen von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) zu, die die aktuellen Einstellungen darstellen, die für diese Objekte gelten. Genauer gesagt ordnet sie [**Msvm \_ ComputerSystem**](msvm-computersystem.md) Instanzen von [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)zu und ordnet **Msvm \_ \** _-Ableitungen von [_ CIM *\_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) **Msvm \_ \** _-Ableitungen von _ CIM [*\_ ResourceAllocationSettingData* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)zu.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SettingsDefineState-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SettingsDefineState-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den virtuellen Computer.

</dd> <dt>

**Settingdata**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf die derzeit aktiven Einstellungen für den virtuellen Computer.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ SettingsDefineState-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-EinstellungenDefineState**](cim-settingsdefinestate.md)
</dt> <dt>

[**\_CIM-EinstellungenDefineState**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Verwaltungsklassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

