---
description: Stellt eine Zuordnung zwischen einem virtuellen System und der aktuellen Momentaufnahme des Systems dar. Diese Zuordnung kann nur vorhanden sein, wenn das virtuelle System mithilfe einer Momentaufnahme erstellt wurde oder eine Momentaufnahme aus dem virtuellen System erstellt wurde.
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
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348313"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a>CIM- \_ Klasse "mustcurrentsnapshotinbranch"

Stellt eine Zuordnung zwischen einem virtuellen System und der aktuellen Momentaufnahme des Systems dar. Diese Zuordnung kann nur vorhanden sein, wenn das virtuelle System mithilfe einer Momentaufnahme erstellt wurde oder eine Momentaufnahme aus dem virtuellen System erstellt wurde.

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

Die CIM-Klasse " **\_ mustcurrentsnapshotinbranch** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ mustcurrentsnapshotinbranch** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf die Instanz des [**CIM- \_ Computer Systems**](cim-computersystem.md) , das das virtuelle System darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ virtualsystemsettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf die Instanz von [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) , die die Momentaufnahme des virtuellen Systems darstellt.

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

 

