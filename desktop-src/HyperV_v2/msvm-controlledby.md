---
description: Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b08cf97c54363009e839ea78fe139c6c8a1bdd81cac07182d019d3d00857dee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130600"
---
# <a name="msvm_controlledby-class"></a>Msvm \_ ControlledBy-Klasse

Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu. Diese Zuordnung wird sowohl mit IDE- als auch mit Diskettencontrollern verwendet.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ControlledBy-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ControlledBy-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zugriff auf das Gerät über den yedent-Controller. Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt**](/windows/desktop/CIMWin32Prov/cim-controlledby)und immer auf 2 (Lesen/Schreiben) festgelegt.

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Priorität, die den Zugriffen des Geräts über diesen Controller erteilt wird. Der Pfad mit der höchsten Priorität hat den niedrigsten Wert. Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt**](/windows/desktop/CIMWin32Prov/cim-controlledby)und immer auf 0 festgelegt.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv befehlet oder auf das Gerät zutritt. Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt**](/windows/desktop/CIMWin32Prov/cim-controlledby)und immer auf 1 (Aktiv) festgelegt.

</dd> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ CIM-Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den Controller. Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf das gesteuerte Gerät. Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse des zugeordneten Geräts im Kontext des Vordenkcontrollers. Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ DeviceConnection geerbt**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)und immer auf 0 festgelegt.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ DeviceConnection geerbt**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)und immer auf 0 festgelegt.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt,**](/windows/desktop/CIMWin32Prov/cim-controlledby)aber nicht verwendet.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt,**](/windows/desktop/CIMWin32Prov/cim-controlledby)aber nicht verwendet.

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt,**](/windows/desktop/CIMWin32Prov/cim-controlledby)aber nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ControlledBy-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

