---
description: Eine Zuordnung zwischen einer Instanz von Msvm \_ VirtualSystemSettingData und der Msvm \_ VirtualSystemSettingData-Instanz, die die letzte Momentaufnahme darstellt, auf der dieses Objekt basiert.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Msvm_ParentChildSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e11f8646988a8cb1d963bd4cc45901f42ffef7525cfa9d228cc8de5c0dfa3c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147391"
---
# <a name="msvm_parentchildsettingdata-class"></a>Msvm \_ ParentChildSettingData-Klasse

Eine Zuordnung zwischen einer Instanz von [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) und der **Msvm \_ VirtualSystemSettingData-Instanz,** die die letzte Momentaufnahme darstellt, auf der dieses Objekt basiert.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ParentChildSettingData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ParentChildSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Die Momentaufnahmeeinstellungsdaten, auf denen die untergeordneten Einstellungsdaten basieren.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Die Einstellungsdaten für den virtuellen Computer, der das untergeordnete Element des übergeordneten Computers darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ParentChildSettingData-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[**\_CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[Virtuelle Systemklassen](virtual-system-classes.md)
</dt> </dl>

 

