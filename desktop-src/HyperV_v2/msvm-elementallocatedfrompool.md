---
description: Ordnet dem Ressourcenpool, aus dem Sie zugewiesen wurde, eine Instanz einer zugeordneten Ressource zu.
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
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349970"
---
# <a name="msvm_elementallocatedfrompool-class"></a>MSVM \_ elementenumeredfrompool-Klasse

Ordnet dem Ressourcenpool, aus dem Sie zugewiesen wurde, eine Instanz einer zugeordneten Ressource zu.

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

Die **MSVM- \_ elementzuzuklasse** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ elementdeperedfrompool** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **außer Kraft** setzung, **Max** (1)
</dt> </dl>

Der Ressourcenpool. Diese Eigenschaft wird von [**CIM \_ elementzuzuedfrompool**](/previous-versions//cc150668(v=vs.85))geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die zugeordnete Ressource. Diese Eigenschaft wird von [**CIM \_ elementzuzuedfrompool**](/previous-versions//cc150668(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ elementzugedfrompool** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ elementzuzuedfrompool**](cim-elementallocatedfrompool.md)
</dt> <dt>

[**CIM \_ elementzuzuedfrompool**](/previous-versions//cc150668(v=vs.85))
</dt> <dt>

[**MSVM \_ Element Zuordnung (v1)**](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[Ressourcen Verwaltungs Klassen](resource-management-classes.md)
</dt> </dl>

 

