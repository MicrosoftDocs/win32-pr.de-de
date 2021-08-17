---
description: Ordnet eine Instanz einer zugeordneten Ressource dem Ressourcenpool zu, aus dem sie zugeordnet wurde.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Msvm_ElementAllocatedFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a68731bec7ae7ab8126fa6b76305257d4333f06012e619cd7a3c9a90bcc69283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148532"
---
# <a name="msvm_elementallocatedfrompool-class"></a>\_Msvm-ElementAllocatedFromPool-Klasse

Ordnet eine Instanz einer zugeordneten Ressource dem Ressourcenpool zu, aus dem sie zugeordnet wurde.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ElementAllocatedFromPool-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ Msvm-Klasse ElementAllocatedFromPool** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Überschreiben** von , **Max** (1)
</dt> </dl>

Der Ressourcenpool. Diese Eigenschaft wird von [**CIM \_ ElementAllocatedFromPool geerbt.**](/previous-versions//cc150668(v=vs.85))

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die zugeordnete Ressource. Diese Eigenschaft wird von [**CIM \_ ElementAllocatedFromPool geerbt.**](/previous-versions//cc150668(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **\_ Msvm-Klasse ElementAllocatedFromPool** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-ElementAllocatedFromPool**](cim-elementallocatedfrompool.md)
</dt> <dt>

[**\_CIM-ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))
</dt> <dt>

[**Msvm \_ ElementAllocatedFromPool (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[Ressourcenverwaltungsklassen](resource-management-classes.md)
</dt> </dl>

 

