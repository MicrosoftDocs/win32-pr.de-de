---
description: Ordnet dem Ressourcenpool, aus dem sie zugeordnet wird, eine Instanz einer Ressourcenzuordnung zu.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Msvm_ResourceAllocationFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8d3913f03560262309084d99ea97b44a165944d4b71acdcac17e2a39bfd44a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148203"
---
# <a name="msvm_resourceallocationfrompool-class"></a>Msvm \_ ResourceAllocationFromPool-Klasse

Ordnet dem Ressourcenpool, aus dem sie zugeordnet wird, eine Instanz einer Ressourcenzuordnung zu.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ResourceAllocationFromPool-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ResourceAllocationFromPool-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Überschreiben von**, **Max.** (1)
</dt> </dl>

Der Ressourcenpool. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Ressourcenzuordnung. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ResourceAllocationFromPool-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ResourceAllocationFromPool**](cim-resourceallocationfrompool.md)
</dt> <dt>

[**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))
</dt> <dt>

[**Msvm \_ ResourceAllocationFromPool (V1)**](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[Ressourcenverwaltungsklassen](resource-management-classes.md)
</dt> </dl>

 

