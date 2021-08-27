---
description: Ordnet einem seriellen Controller einen seriellen Anschluss zu.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ddc5a5c006b92945178f89cf5f4df585f96ed3eaef692b04326878cb0d16520
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107440"
---
# <a name="msvm_serialportonserialcontroller-class"></a>Msvm \_ SerialPortOnSerialController-Klasse

Ordnet einem seriellen Controller einen seriellen Anschluss zu.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SerialPortOnSerialController-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SerialPortOnSerialController-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der serielle Controller, mit dem der Port verbunden ist. Diese Eigenschaft wird von [**CIM \_ PortOnDevice geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anschluss des seriellen Controllers. Diese Eigenschaft wird von [**CIM \_ PortOnDevice geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ SerialPortOnSerialController-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**\_CIM-PortOnGeräte**](cim-portondevice.md)
</dt> <dt>

[**\_CIM-PortOnGeräte**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Klassen für serielle Geräte](serial-devices-classes.md)
</dt> </dl>

 

