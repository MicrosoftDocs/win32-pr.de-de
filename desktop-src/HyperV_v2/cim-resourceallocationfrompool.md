---
description: Stellt eine Zuordnung dar, in der eine CIM \_ resourcezucationsettingdata-Instanz aus einem Ressourcenpool zugewiesen wird.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: CIM_ResourceAllocationFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960274"
---
# <a name="cim_resourceallocationfrompool-class"></a>CIM \_ resourcezucationfrompool-Klasse

Stellt eine Zuordnung dar, in der eine [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Instanz aus einem Ressourcenpool zugewiesen wird.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Member

Die **CIM \_ resourcezucationfrompool** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ resourcezucationfrompool** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ resourcepool**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Der Ressourcenpool.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ resourcezubesettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Die Ressourcen Zuordnungs Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

