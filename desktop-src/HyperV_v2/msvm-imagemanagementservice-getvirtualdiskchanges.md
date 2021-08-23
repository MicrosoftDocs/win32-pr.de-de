---
description: Ruft eine Liste der Änderungen in der angegebenen Region eines virtuellen Datenträgers ab, die seit der bereitgestellten resilienten Änderungsnachverfolgung oder VHDSet-Momentaufnahme-ID vorgenommen wurden.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: GetVirtualDiskChanges-Methode der Msvm_ImageManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8b96c5b4d2bbdff78b6f9f2bc9a1e7547742a553564e0f81547b8d998f86f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522560"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>GetVirtualDiskChanges-Methode der Msvm \_ ImageManagementService-Klasse

Ruft eine Liste der Änderungen in der angegebenen Region eines virtuellen Datenträgers ab, die seit der bereitgestellten resilienten Änderungsnachverfolgung oder VHDSet-Momentaufnahme-ID vorgenommen wurden.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ In\]
</dt> <dd>

Ein vollqualifizierter Pfad, der den Speicherort der Datei für die virtuelle Festplatte angibt.

</dd> <dt>

*LimitId* \[ In\]
</dt> <dd>

Eine resiliente Änderungsnachverfolgung ID oder VHD Set Snapshot ID, die die Baseline für Änderungen auf dem virtuellen Datenträger angibt.

</dd> <dt>

*TargetSnapshotId* \[ In\]
</dt> <dd>

Eine VHDSet-Momentaufnahme-ID, die die Momentaufnahme angibt, die mit der Baseline verglichen werden soll, wenn Änderungen in der virtuellen Festplatte bestimmt werden. Dieser Parameter ist nur für VHD-Set-Dateien gültig.

</dd> <dt>

*ByteOffset* \[ In\]
</dt> <dd>

Der Byteoffset der Region auf dem virtuellen Datenträger, nach dem Änderungen abfragt werden.

</dd> <dt>

*ByteLength* \[ In\]
</dt> <dd>

Die Bytelänge der Region auf dem virtuellen Datenträger, nach der Änderungen abfragt werden. Dieser muss kleiner als die Größe des virtuellen Datenträgers sein.

</dd> <dt>

*ProcessedByteLength* \[ out\]
</dt> <dd>

Die gesamte Bytelänge, die verarbeitet wurde. Dies kann byteLength oder kleiner sein.

</dd> <dt>

*ChangedByteOffsets* \[ out\]
</dt> <dd>

Die Liste der Byteoffsets auf dem virtuellen Datenträger, die den Anfang jedes geänderten Bereichs angeben.

</dd> <dt>

*ChangedByteLengths* \[ out\]
</dt> <dd>

Die Liste der Bytelängen der geänderten Bereiche auf dem virtuellen Datenträger.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn der Task abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger** Parameter (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




