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
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373276"
---
# <a name="msvm_controlledby-class"></a>MSVM \_ controlledby-Klasse

Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu. Diese Zuordnung wird sowohl für IDE als auch für Disketten Controller verwendet.

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

Die **MSVM \_ controlledby** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ controlledby** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zugriff auf das Gerät über den Vorgänger Controller. Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt und ist immer auf 2 festgelegt (Lese-/Schreibzugriff).

</dd> <dt>

**Accesspriority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Priorität, die für den Zugriff auf das Gerät über diesen Controller eingeräumt wird. Der Pfad mit der höchsten Priorität hat den niedrigsten Wert. Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt und ist immer auf 0 festgelegt.

</dd> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift. Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt und ist immer auf 1 (aktiv) festgelegt.

</dd> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den Controller. Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf das kontrollierte Gerät. Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt.

</dd> <dt>

**Devicengegen ber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse des zugeordneten Geräts im Zusammenhang mit dem Vorgänger Controller. Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt.

</dd> <dt>

**Aushandateddatawidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von CIM-Geräte [**\_ Bindung**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)geerbt und immer auf 0 festgelegt.

</dd> <dt>

**Aushandatedspeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von CIM-Geräte [**\_ Bindung**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)geerbt und immer auf 0 festgelegt.

</dd> <dt>

**Anzahlersätze**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt, aber nicht verwendet.

</dd> <dt>

**Anzahlermengen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt, aber nicht verwendet.

</dd> <dt>

**Timeofdevicereset**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt, aber nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ controlledby** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ controlledby**](cim-controlledby.md)
</dt> <dt>

[**CIM- \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Speicher Klassen](storage-classes.md)
</dt> </dl>

 

