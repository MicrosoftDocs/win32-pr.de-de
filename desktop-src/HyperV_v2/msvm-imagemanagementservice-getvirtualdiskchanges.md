---
description: Ruft eine Liste der Änderungen im angegebenen Bereich eines virtuellen Datenträgers ab, die von der angegebenen robusten Änderungsnachverfolgung ID oder der vhdset-Momentaufnahme-ID bereitgestellt werden.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Getvirtualdiskchanges-Methode der Msvm_ImageManagementService-Klasse
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
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353118"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Getvirtualdiskchanges-Methode der MSVM \_ imagemanagementservice-Klasse

Ruft eine Liste der Änderungen im angegebenen Bereich eines virtuellen Datenträgers ab, die von der angegebenen robusten Änderungsnachverfolgung ID oder der vhdset-Momentaufnahme-ID bereitgestellt werden.

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

*Pfad* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der virtuellen Festplatten Datei angibt.

</dd> <dt>

*Limitid* \[ in\]
</dt> <dd>

Eine robuste Änderungsnachverfolgung ID oder eine Momentaufnahme-ID des VHD-Satzes, die die Baseline für Änderungen auf dem virtuellen Datenträger angibt.

</dd> <dt>

*Targetinapshotid* \[ in\]
</dt> <dd>

Eine vhdset-Momentaufnahme-ID, die die Momentaufnahme angibt, die beim determinimieren der virtuellen Festplatte mit der Baseline verglichen werden soll. Dieser Parameter ist nur für VHD-Set-Dateien gültig.

</dd> <dt>

*Byteoffset* \[ in\]
</dt> <dd>

Der Byte Offset der Region im virtuellen Datenträger, für die Änderungen abgefragt werden sollen.

</dd> <dt>

*ByteLength* \[ in\]
</dt> <dd>

Die Byte Länge der Region im virtuellen Datenträger, für die Änderungen abgefragt werden sollen. Diese muss kleiner als die Größe des virtuellen Datenträgers sein.

</dd> <dt>

*Processedbytelength* \[ vorgenommen\]
</dt> <dd>

Die gesamte Byte Länge, die verarbeitet wurde. Dieser Wert kann gleich ByteLength oder kleiner sein.

</dd> <dt>

*Changedbyteoffsets* \[ vorgenommen\]
</dt> <dd>

Die Liste der Byte Offsets in der virtuellen Festplatte, die den Anfang jedes geänderten Bereichs angibt.

</dd> <dt>

*Changedbytelengths* \[ vorgenommen\]
</dt> <dd>

Die Liste der Byte Längen der geänderten Bereiche auf dem virtuellen Datenträger.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
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

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




