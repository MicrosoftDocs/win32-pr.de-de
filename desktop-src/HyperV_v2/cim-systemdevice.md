---
description: Ordnet ein System einem logischen Gerät zu, das eine Komponente des Systems ist.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: CIM_SystemDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e45c2ffabe477a7a3908102b32e4257f6bb54bbcb9e85f80e6b894021173310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899450"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a>CIM_SystemDevice-Klasse (Hyper-V-Verwaltung)

Ordnet ein System einem logischen Gerät zu, das eine Komponente des Systems ist.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a>Member

Die **\_ CIM-SystemDevice-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-SystemDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-System**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregieren,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**\_ CIM-Systemverweis**](cim-system.md) auf das übergeordnete System in der Zuordnung.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein [**CIM \_ LogicalDevice-Verweis**](cim-logicaldevice.md) auf das logische Gerät, das eine Komponente des Systems ist.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> </dl>

 

