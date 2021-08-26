---
description: Überprüft die Kompatibilitätsinformationen auf Kompatibilität mit dem Hostcomputersystem.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: CheckSystemCompatibilityInfo-Methode der Msvm_VirtualSystemMigrationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7492d3f7dcdc20abca5cd574d1006b5e2090d02d28f7446dd94ec7b777541b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041980"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>CheckSystemCompatibilityInfo-Methode der Msvm \_ VirtualSystemMigrationService-Klasse

Überprüft die Kompatibilitätsinformationen auf Kompatibilität mit dem Hostcomputersystem.

## <a name="syntax"></a>Syntax


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CompatibilityInfo* \[ In\]
</dt> <dd>

Ein Blob von Daten, das durch Aufrufen der [**GetSystemCompatibilityInfo-Methode**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) auf dem Hostcomputersystem ermittelt wird.

</dd> <dt>

*Gründe* \[ out\]
</dt> <dd>

Ein Array von Zeichenfolgen, das die eingebetteten Instanzen der [**Msvm \_ Error-Klasse**](msvm-error.md) empfängt, die alle Warnungen oder Fehler darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

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

**Nicht kompatibel** (32784)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




