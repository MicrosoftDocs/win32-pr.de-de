---
description: Stellt eine Zuordnung zwischen einer Instanz von Msvm \_ ComputerSystem dar, die den virtuellen Computer darstellt, und einer Instanz von Msvm \_ ReplicationRelationship, die eine Replikationsbeziehung des virtuellen Computers darstellt.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86040e6dc5676f6cd40b223f0a3cbd31864965722de957fda6ff1d140ad94b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810606"
---
# <a name="msvm_systemreplicationrelationship-class"></a>Msvm \_ SystemReplicationRelationship-Klasse

Stellt eine Zuordnung zwischen einer Instanz von [**Msvm \_ ComputerSystem**](msvm-computersystem.md) dar, die den virtuellen Computer darstellt, und einer Instanz von [**Msvm \_ ReplicationRelationship,**](msvm-replicationrelationship.md) die eine Replikationsbeziehung des virtuellen Computers darstellt. Diese Klasse wird von der [**\_ CIM-Abhängigkeitsklasse**](/windows/desktop/CIMWin32Prov/cim-dependency) abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SystemReplicationRelationship-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SystemReplicationRelationship-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Verweis auf die Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die den virtuellen Computer darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ ReplicationRelationship**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Verweis auf die Instanz der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) die die Replikationsbeziehung eines virtuellen Systems darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[**\_CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

