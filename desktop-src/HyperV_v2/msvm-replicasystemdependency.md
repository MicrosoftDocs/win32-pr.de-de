---
description: Stellt eine Zuordnung zwischen einer Instanz der CIM ComputerSystem-Klasse dar, die das Replikat des virtuellen Computers darstellt, und einer Instanz der CIM ComputerSystem-Klasse, die das Replikat des \_ \_ virtuellen Testcomputers darstellt.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Msvm_ReplicaSystemDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f6bb3f4879ee0e1c7babaf8f85b8455716ee1b2e61db4e0764d6b28583efefd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130430"
---
# <a name="msvm_replicasystemdependency-class"></a>Msvm \_ ReplicaSystemDependency-Klasse

Stellt eine Zuordnung zwischen einer Instanz der [**CIM \_ ComputerSystem-Klasse**](/windows/desktop/CIMWin32Prov/cim-computersystem) dar, die das Replikat des virtuellen Computers darstellt, und einer Instanz der **CIM \_ ComputerSystem-Klasse,** die das Replikat des virtuellen Testcomputers darstellt.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ReplicaSystemDependency-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ReplicaSystemDependency-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**\_ CIM-ComputerSystem-Klasse,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die das Replikat des virtuellen Computers darstellt. Diese Eigenschaft wird von der [**CIM-Abhängigkeit \_ geerbt.**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**\_ CIM-ComputerSystem-Klasse,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die das von der [**Msvm \_ ReplicationService.TestReplicaSystem-Methode**](testreplicasystem-msvm-replicationservice.md) erstellte Testreplikat des virtuellen Computers darstellt. Diese Eigenschaft wird von der [**CIM-Abhängigkeit \_ geerbt.**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

