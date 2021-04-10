---
description: Stellt einen Teil einer Beziehung zwischen einer CIM \_ -virtualsystemsettingdata-Instanz und einem Satz von CIM \_ resourcezucationsettingdata-Instanzen dar.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: CIM_VirtualSystemSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132000"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a>CIM \_ virtualsystemsettingdatacomponent-Klasse

Stellt einen Teil einer Beziehung zwischen einer [**CIM- \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Instanz und einem Satz von [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Instanzen dar.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Member

Die **CIM- \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ virtualsystemsettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ein Verweis auf das [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Objekt der obersten Ebene der virtuellen Systemkonfiguration.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ resourcezubesettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf das [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Objekt, das einen Teil der Konfiguration des virtuellen Systems darstellt.

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

[**CIM- \_ Komponente**](cim-component.md)
</dt> </dl>

 

