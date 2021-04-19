---
description: Ordnet eine Instanz der MSVM \_ Computersystem-oder MSVM \_ plannedcomputersystem-Klasse zu, die ein virtuelles System darstellt, mit einer Instanz der MSVM \_ virtualsystemsettingdata-Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die die aktuellste Momentaufnahme in einer Verzweigung abhängiger Momentaufnahmen ist.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Msvm_MostCurrentSnapshotInBranch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352731"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a>MSVM- \_ Klasse "mustcurrentsnapshotinbranch"

Ordnet eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -oder [**MSVM \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Klasse zu, die ein virtuelles System darstellt, mit einer Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die die aktuellste Momentaufnahme in einer Verzweigung abhängiger Momentaufnahmen ist.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM-Klasse " \_ mustcurrentsnapshotinbranch** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ mustcurrentsnapshotinbranch** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -oder [**MSVM \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Klasse, die das virtuelle System darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die die aktuellste Momentaufnahme in einer Verzweigung abhängiger Momentaufnahmen ist. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

