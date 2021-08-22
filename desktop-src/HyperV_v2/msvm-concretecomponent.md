---
description: Eine generische Zuordnung, die verwendet wird, um einen Teil der Beziehungen zwischen verwalteten Elementen zu erstellen.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24b813e7b8460f3de24207ed91b2e113f0d6b9633e17263806ef8447c166bdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531750"
---
# <a name="msvm_concretecomponent-class"></a>Msvm \_ ConcreteComponent-Klasse

Eine generische Zuordnung, die verwendet wird, um "Teil von"-Beziehungen zwischen verwalteten Elementen zu erstellen. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) ist als konkrete Unterklasse der abstrakten [**\_ CIM-Komponentenklasse**](/windows/desktop/CIMWin32Prov/cim-component) definiert, die statt vieler spezifischer Unterklassen von Komponenten verwendet werden soll, die keine Semantik hinzufügen (d. h. Unterklassen, die nicht den Typ der Komposition verdeutlichen, Kardinalitäten aktualisieren oder Qualifizierer hinzufügen oder entfernen).

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ConcreteComponent-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ConcreteComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element in der Zuordnung. Diese Eigenschaft wird von [**CIM \_ ConcreteComponent geerbt.**](/previous-versions//cc150665(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das untergeordnete Element in der Zuordnung. Diese Eigenschaft wird von [**CIM \_ ConcreteComponent geerbt.**](/previous-versions//cc150665(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ConcreteComponent-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ConcreteComponent**](cim-concretecomponent.md)
</dt> <dt>

[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Virtuelle Systemklassen](virtual-system-classes.md)
</dt> </dl>

 

