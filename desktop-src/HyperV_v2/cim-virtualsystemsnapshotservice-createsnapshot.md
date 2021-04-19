---
description: Erstellt eine Momentaufnahme eines virtuellen Systems.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Kreatesnapshot-Methode der CIM_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356930"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Kreatesnapshot-Methode der CIM \_ virtualsystemsnapshotservice-Klasse

Erstellt eine Momentaufnahme eines virtuellen Systems.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedsystem* \[ in\]
</dt> <dd>

Ein [**CIM \_ Computersystem**](cim-computersystem.md) -Verweis auf das betroffene virtuelle System.

</dd> <dt>

*Snapshotsettings* \[ in\]
</dt> <dd>

Parameter Einstellungen.

</dd> <dt>

*Snapshottype* \[ in\]
</dt> <dd>

Angeforderter snapshottyp:

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Vollständige Momentaufnahme** (2)


</dt> <dd>

Vervollständigen Sie die Momentaufnahme des virtuellen Systems.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>Datenträger **Momentaufnahme** (3)


</dt> <dd>

Momentaufnahme von virtuellen System Datenträgern.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Resultingsnapshot* \[ in, out\]
</dt> <dd>

Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Verweis auf die resultierende virtuelle System Momentaufnahme.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall gilt: die Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse, die die neue Momentaufnahme des virtuellen Systems darstellt, wird über die [**CIM \_ affectedjobelate**](cim-affectedjobelement.md) -Zuordnung mit dem Wert der **affectedelta** -Eigenschaft präsentiert, die auf die neue Instanz der **CIM \_ virtualsystemsettingdata** -Klasse verweist, die  die Momentaufnahme des virtuellen Systems darstellt

> [!Note]  
> Dieser Parameter war in Windows 8.1 mit Lese-/Schreibzugriff.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Status** (5)
</dt> <dt>

**Ungültiger Typ** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemsnapshotservice**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




