---
description: Stellt eine Zuordnung zwischen einer Instanz von MSVM \_ Computersystem dar, die den virtuellen Computer und eine Instanz von MSVM \_ replicationrelationship darstellt, die eine Replikations Beziehung des virtuellen Computers darstellt.
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
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958744"
---
# <a name="msvm_systemreplicationrelationship-class"></a>MSVM \_ systemreplicationrelationship-Klasse

Stellt eine Zuordnung zwischen einer Instanz von [**MSVM \_ Computersystem**](msvm-computersystem.md) dar, die den virtuellen Computer und eine Instanz von [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) darstellt, die eine Replikations Beziehung des virtuellen Computers darstellt. Diese Klasse wird von der [**CIM- \_ Abhängigkeits**](/windows/desktop/CIMWin32Prov/cim-dependency) Klasse abgeleitet.

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

Die **MSVM \_ systemreplicationrelationship** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ systemreplicationrelationship** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")
</dt> </dl>

Verweis auf die Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ replicationrelationship**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")
</dt> </dl>

Verweis auf die Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die Replikations Beziehung eines virtuellen Systems darstellt.

</dd> </dl>

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

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

