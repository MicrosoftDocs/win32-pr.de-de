---
description: Stellt eine Zuordnung zwischen einem virtuellen System und der aktuellen Momentaufnahme des Systems dar. Diese Zuordnung kann nur vorhanden sein, wenn das virtuelle System mithilfe einer Momentaufnahme erstellt wurde oder wenn eine Momentaufnahme aus dem virtuellen System erstellt wurde.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: CIM_MostCurrentSnapshotInBranch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: de94bf0e6f88240ac89eb62de881540f5c747b7a1d0ec13307e7e5d35fe53da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694970"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a>CIM \_ MostCurrentSnapshotInBranch-Klasse

Stellt eine Zuordnung zwischen einem virtuellen System und der aktuellen Momentaufnahme des Systems dar. Diese Zuordnung kann nur vorhanden sein, wenn das virtuelle System mithilfe einer Momentaufnahme erstellt wurde oder wenn eine Momentaufnahme aus dem virtuellen System erstellt wurde.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Member

Die **CIM \_ MostCurrentSnapshotInBranch-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ MostCurrentSnapshotInBranch-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf die Instanz von [**CIM \_ ComputerSystem,**](cim-computersystem.md) die das virtuelle System darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf die Instanz von [**CIM \_ VirtualSystemSettingData,**](cim-virtualsystemsettingdata.md) die die Momentaufnahme des virtuellen Systems darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

