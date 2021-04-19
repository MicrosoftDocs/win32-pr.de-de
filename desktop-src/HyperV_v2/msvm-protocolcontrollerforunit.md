---
description: Diese Zuordnung gibt an, dass eine Unterklasse des logischen Geräts (z. b. ein Speicher Volume) über einen bestimmten Protokoll Controller verbunden ist.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345854"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>MSVM \_ protocolcontrollerforunit-Klasse

Diese Zuordnung gibt an, dass eine Unterklasse des logischen Geräts (z. b. ein Speicher Volume) über einen bestimmten Protokoll Controller verbunden ist. In vielen Situationen (z. b. bei der Speicher-LUN-Maskierung) können viele dieser Zuordnungen verwendet werden, um sich auf unterschiedliche Objekte zu beziehen. Daher wurden Unterklassen definiert, um die Enumeration der Zuordnungen zu optimieren.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Member

Die **MSVM \_ protocolcontrollerforunit** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ protocolcontrollerforunit** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Accesspriority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Priorität, die für den Zugriff auf das Gerät über diesen Controller eingeräumt wird. Der Pfad mit der höchsten Priorität weist den niedrigsten Wert für diesen Parameter auf. Diese Klasse wird von **CIM \_ protocolcontrollerfordevice** geerbt.

</dd> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv auf das Gerät zugreift (2) oder nicht (3). Außerdem kann der Wert 0 (unbekannt) definiert werden. Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Protokoll Controller oder durch den Zugriff darauf zugegriffen werden kann. Diese Klasse wird von **CIM \_ protocolcontrollerfordevice** geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Aktiv** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inaktiv** (3)
</dt> </dl>

</dd> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ protocolcontroller**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Protokoll Controller. Diese Klasse wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das kontrollierte Gerät. Diese Klasse wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Deviceaccess**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zugriffsrechte, die dem Gerät über diesen Controller erteilt wurden. Diese Klasse wird von **CIM \_ protocolcontrollerforunit** geerbt.



| Wert                                                                               | Bedeutung                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unbekannt<br/>         |
| <dl> <dt>2</dt> </dl>        | Lesen/Schreiben<br/>      |
| <dl> <dt>3</dt> </dl>        | Schreibgeschützt<br/>       |
| <dl> <dt>4</dt> </dl>        | Kein Zugriff.<br/>      |
| <dl> <dt>5.. 15999</dt> </dl> | DMTF reserviert<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Anbieter reserviert<br/> |



 

</dd> <dt>

**Devicengegen ber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse des zugeordneten Geräts im Zusammenhang mit dem Vorgänger Controller. Diese Klasse wird von **CIM \_ protocolcontrollerfordevice** geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ protocolcontrollerforunit** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ protocolcontrollerforunit**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**CIM \_ protocolcontrollerforunit**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Speicher Klassen](storage-classes.md)
</dt> </dl>

 

