---
description: Ordnet einem virtuellen System eine Momentaufnahme zu, die vom virtuellen System erfasst wurde.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959277"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a>MSVM \_ snapshodessystem-Klasse

Ordnet einem virtuellen System eine Momentaufnahme zu, die vom virtuellen System erfasst wurde.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ snapshotofvirtualsystem** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ snapshodessystem** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das virtuelle System darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.

</dd> </dl>

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

[**CIM \_ snapshoto-virtualsystem**](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[**CreateSnapshot**](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

