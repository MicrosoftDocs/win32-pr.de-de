---
description: Diese Zuordnung gibt an, dass eine Unterklasse eines logischen Geräts (z. B. ein Speichervolume) über einen bestimmten Protokollcontroller verbunden ist.
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
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086630"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>Msvm \_ ProtocolControllerForUnit-Klasse

Diese Zuordnung gibt an, dass eine Unterklasse eines logischen Geräts (z. B. ein Speichervolume) über einen bestimmten Protokollcontroller verbunden ist. In vielen Situationen (z. B. bei der Speicher-LUN-Maskierung) können viele dieser Zuordnungen verwendet werden, um sich auf verschiedene Objekte zu beziehen. Daher wurden Unterklassen definiert, um die Enumeration der Zuordnungen zu optimieren.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ ProtocolControllerForUnit-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ProtocolControllerForUnit-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Priorität für den Zugriff auf das Gerät über diesen Controller. Der Pfad mit der höchsten Priorität weist den niedrigsten Wert für diesen Parameter auf. Diese Klasse wird von **CIM \_ ProtocolControllerForDevice** geerbt.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv auf das Gerät (2) oder nicht (3) zugreift. Außerdem kann der Wert 0 (Unbekannt) definiert werden. Diese Informationen sind erforderlich, wenn ein logisches Gerät von mehreren Protokollcontrollern befehlsgesteuert oder über diesen aufgerufen werden kann. Diese Klasse wird von **CIM \_ ProtocolControllerForDevice** geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Aktiv** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inaktiv** (3 )
</dt> </dl>

</dd> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Protokollcontroller. Diese Klasse wird von [**\_ CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das kontrollierte Gerät. Diese Klasse wird von [**\_ CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zugriffsrechte, die dem Gerät über diesen Controller gewährt werden. Diese Klasse wird von **CIM \_ ProtocolControllerForUnit** geerbt.



| Wert                                                                               | Bedeutung                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unbekannt<br/>         |
| <dl> <dt>2</dt> </dl>        | Lesen/Schreiben<br/>      |
| <dl> <dt>3</dt> </dl>        | Schreibgeschützt<br/>       |
| <dl> <dt>4</dt> </dl>        | Kein Zugriff.<br/>      |
| <dl> <dt>5..15999</dt> </dl> | DMTF reserviert<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Reservierter Anbieter<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse des zugeordneten Geräts im Kontext des Vorgängercontrollers. Diese Klasse wird von **CIM \_ ProtocolControllerForDevice** geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ProtocolControllerForUnit-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ProtocolControllerForUnit**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**CIM \_ ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

