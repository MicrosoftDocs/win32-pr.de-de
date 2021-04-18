---
description: Eine generische Zuordnung, die verwendet wird, um einen Teil der Beziehungen zwischen verwalteten Elementen herzustellen.
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
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347464"
---
# <a name="msvm_concretecomponent-class"></a>MSVM- \_ Klasse "concretecomponent"

Eine generische Zuordnung, die verwendet wird, um Beziehungen zwischen verwalteten Elementen herzustellen. [**CIM \_ "Concretecomponent**](/previous-versions//cc150665(v=vs.85)) " ist als konkrete Unterklasse der abstrakten [**CIM- \_ Komponenten**](/windows/desktop/CIMWin32Prov/cim-component) Klasse definiert und kann anstelle vieler spezifischer Unterklassen von Komponenten verwendet werden, die keine Semantik hinzufügen (d. h. Unterklassen, die den Typ der Komposition nicht verdeutlichen, Kardinalitäten aktualisieren oder Qualifizierer hinzufügen oder entfernen).

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

Die **MSVM-Klasse " \_ concretecomponent** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ concretecomponent** " verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element in der Zuordnung. Diese Eigenschaft wird von [**CIM " \_ concretecomponent**](/previous-versions//cc150665(v=vs.85))" geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das untergeordnete-Element in der Zuordnung. Diese Eigenschaft wird von [**CIM " \_ concretecomponent**](/previous-versions//cc150665(v=vs.85))" geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM-Klasse " \_ concretecomponent** " kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ concretecomponent**](cim-concretecomponent.md)
</dt> <dt>

[**CIM- \_ concretecomponent**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Klassen des virtuellen Systems](virtual-system-classes.md)
</dt> </dl>

 

