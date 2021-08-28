---
description: Überprüft, ob ein Dateisystem eine virtuelle Festplatte mit aktivierten persistenten Reservierungen unterstützen kann.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: ValidatePersistentReservationSupport-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f1384ca9b56c24a40925a08fb87595fd57acef3e50c1d5d09593d9cfd7f545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147722"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a>ValidatePersistentReservationSupport-Methode der Msvm \_ ImageManagementService-Klasse

Überprüft, ob ein Dateisystem eine virtuelle Festplatte mit aktivierten persistenten Reservierungen unterstützen kann.

## <a name="syntax"></a>Syntax


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ In\]
</dt> <dd>

Ein vollqualifizierter Pfad, der den Speicherort einer Datenträgerimagedatei oder eines Verzeichnisses angibt, in dem eine Datenträgerimagedatei platziert werden kann.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe erfolgreich abgeschlossen wurde).

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
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




