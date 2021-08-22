---
description: Erstellt eine Momentaufnahme eines virtuellen Systems.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: CreateSnapshot-Methode der CIM_VirtualSystemSnapshotService Klasse
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
ms.openlocfilehash: 8ee1a2e66745ceac50cc00ba6e625a171f18c7d2b54d4e51af2c86f6711675ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532750"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>CreateSnapshot-Methode der CIM \_ VirtualSystemSnapshotService-Klasse

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

*AffectedSystem* \[ In\]
</dt> <dd>

Ein [**\_ CIM-ComputerSystemverweis**](cim-computersystem.md) auf das betroffene virtuelle System.

</dd> <dt>

*SnapshotSettings* \[ In\]
</dt> <dd>

Parametereinstellungen.

</dd> <dt>

*SnapshotType* \[ In\]
</dt> <dd>

Angeforderter Momentaufnahmetyp:

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Vollständige Momentaufnahme** (2)


</dt> <dd>

Vollständige Momentaufnahme des virtuellen Systems.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Datenträgermomentaufnahme** (3)


</dt> <dd>

Momentaufnahme virtueller Systemdatenträger.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Herstellerspezifisch** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[ in, out\]
</dt> <dd>

Ein [**CIM \_ VirtualSystemSettingData-Verweis**](cim-virtualsystemsettingdata.md) auf die resultierende Momentaufnahme des virtuellen Systems.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall wird die Instanz der [**CIM \_ VirtualSystemSettingData-Klasse,**](cim-virtualsystemsettingdata.md) die die neue Momentaufnahme des virtuellen Systems darstellt, über die [**CIM \_ AffectedJobElement-Zuordnung**](cim-affectedjobelement.md) mit dem Wert der **AffectedElement-Eigenschaft** dargestellt, die auf die neue Instanz der **CIM \_ VirtualSystemSettingData-Klasse** verweist, die die Momentaufnahme des virtuellen Systems darstellt, und den Wert der **ElementEffects,** die auf 5 (Create) festgelegt sind.

> [!Note]  
> Dieser Parameter wurde in der -Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Zustand** (5)
</dt> <dt>

**Ungültiger Typ** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ VirtualSystemSnapshotService**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




