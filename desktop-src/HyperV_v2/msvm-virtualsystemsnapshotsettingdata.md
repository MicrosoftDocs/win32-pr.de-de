---
description: Stellt zusätzliche Informationen bereit, die mit der CreateSnapshot-Methode der Msvm \_ VirtualSystemSnapshotService-Klasse verwendet werden.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Msvm_VirtualSystemSnapshotSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d112e4109ed6d0ab899aadf59f0e991f52259eaf2c514c6d9215b04a8cafcab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046250"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a>Msvm \_ VirtualSystemSnapshotSettingData-Klasse

Stellt zusätzliche Informationen bereit, die mit der [**CreateSnapshot-Methode**](cim-virtualsystemsnapshotservice-createsnapshot.md) der [**Msvm \_ VirtualSystemSnapshotService-Klasse**](msvm-virtualsystemsnapshotservice.md) verwendet werden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemSnapshotSettingData-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemSnapshotSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Konsistenzebene der Momentaufnahme.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Anwendungskonsens** (1)


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

**Absturzkons konsistent** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestBackupType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherungstyp, der innerhalb des Gasts verwendet werden soll.

> [!Note]  
> Eigenschaft in Windows 10, Version 1703 hinzugefügt

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Nicht definiert** (0)


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

**Vollständig** (1)


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

**Kopieren** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IgnoreNonSnapshottableDisks**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob nicht momentaufnahmefähige Datenträger wie Passthrough-Datenträger und Fibre Channel Datenträger beim Erstellen der Momentaufnahme ignoriert werden sollen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




