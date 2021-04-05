---
description: Erstellt eine Momentaufnahme einer virtuellen System Sammlung.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Kreatesnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755153"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Die Methode "kreatesnapshot" der Klasse "MSVM \_ collectionsnapshotservice"

Erstellt eine Momentaufnahme einer virtuellen System Sammlung.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sammlung* \[ in\]
</dt> <dd>

Verweis auf einen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) , der die betroffene Sammlung virtueller Systeme beschreibt.

</dd> <dt>

*Snapshotsettings* \[ in\]
</dt> <dd>

Enthält die Parametereinstellungen.

</dd> <dt>

*Snapshottype* \[ in\]
</dt> <dd>

Angeforderter snapshottyp:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Momentaufnahme** (1)


</dt> <dd>

Standard Momentaufnahme des virtuellen Systems.

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Wiederherstellungs Momentaufnahme** (2)


</dt> <dd>

Momentaufnahme für Wiederherstellungs Szenarien, einschließlich failoverreplikation und Sicherung.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Resultingsnapshotcollection* \[ in, out\]
</dt> <dd>

Bei Erfolg wird ein [**CIM- \_ Sammlungs**](cim-collection.md) Verweis mit der Momentaufnahme des virtuellen Systems zurückgegeben.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird entweder 0 (abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ collectionsnapshotservice**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




