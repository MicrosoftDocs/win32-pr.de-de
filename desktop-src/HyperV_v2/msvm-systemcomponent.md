---
description: Richtet eine &\# 0034;Teil von&0034; beziehung zwischen einem System und jedem verwalteten Systemelement ein, aus dem es \# besteht.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Msvm_SystemComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 538deaff8e0edf3d1467c4447a3d25ced18987e4f81bc8d14a056848313c8526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949682"
---
# <a name="msvm_systemcomponent-class"></a>Msvm \_ SystemComponent-Klasse

Richtet eine "Teil von"-Beziehung zwischen einem System und jedem verwalteten Systemelement ein, aus dem es besteht.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SystemComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SystemComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ CIM-System**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element in der Zuordnung. Diese Eigenschaft wird von [**CIM \_ SystemComponent geerbt.**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das untergeordnete Element in der Zuordnung. Diese Eigenschaft wird von [**CIM \_ SystemComponent geerbt.**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

