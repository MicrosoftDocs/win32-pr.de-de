---
description: Ordnet einen virtuellen Computer und seine Geräte Instanzen von CIM \_ SettingData zu, die die aktuellen Einstellungen darstellen, die für diese Objekte gelten.
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
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216764"
---
# <a name="msvm_settingsdefinestate-class"></a>MSVM \_ settingsdefinestate-Klasse

Ordnet einen virtuellen Computer und seine Geräte Instanzen von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) zu, die die aktuellen Einstellungen darstellen, die für diese Objekte gelten. Genauer gesagt, ordnet Sie [**MSVM \_ Computersystem**](msvm-computersystem.md) Instanzen von [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)zu und ordnet **MSVM \_ \** _-Ableitungen von [_ *CIM \_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mit **MSVM \_ \** _-Ableitungen von [_ *CIM \_ resourcezuordcationsettingdata* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)zu.

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

Die **MSVM \_ settingsdefinestate** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ settingsdefinestate** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den virtuellen Computer.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf die derzeit aktiven Einstellungen für den virtuellen Computer.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ settingsdefinestate** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ settingsdefinestate**](cim-settingsdefinestate.md)
</dt> <dt>

[**CIM \_ settingsdefinestate**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Verwaltungs Klassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

