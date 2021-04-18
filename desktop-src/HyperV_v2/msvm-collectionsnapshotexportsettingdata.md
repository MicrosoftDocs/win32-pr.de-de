---
description: Exportieren von Einstellungsdaten, die an die exportsnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse übermittelt werden sollen.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344432"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>MSVM \_ collectionsnapshotexportsettingdata-Klasse

Exportieren von Einstellungsdaten, die an die exportsnapshot-Methode der [**MSVM \_ collectionsnapshotservice**](msvm-collectionsnapshotservice.md) -Klasse übermittelt werden sollen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectionsnapshotexportsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ collectionsnapshotexportsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Backupintent**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Absicht an, wie die exportierten Sicherungs Sätze verwendet werden sollen:

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Backupintentpreservechain** (1)


</dt> <dd>

Alle exportierten vollständigen und differenziellen Sicherungs Sätze werden unverändert beibehalten.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Backupintentmerge** (2)


</dt> <dd>

Die exportierten vollständigen und differenziellen Sicherungs Sätze werden zusammengeführt, um vollständige Sicherungs Sätze zu synthetisieren.

</dd> </dl>

</dd> <dt>

**Copyvmstorage**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wenn der Wert **true** ist, wird der VM-Speicher beim Exportieren des virtuellen Computers kopiert. Andernfalls **false.**

</dd> <dt>

**Differenalbackupbase**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Basis für differenziellen Export. Dies ist entweder ein Pfad zu einer [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) -Instanz, die den Verweis Punkt darstellt, oder ein Pfad zu einer [**MSVM- \_ snapshotcollection**](msvm-snapshotcollection.md) -Instanz, die die Momentaufnahme darstellt, die als Basis für den differenziellen Export verwendet werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




