---
description: Führt einen Neusynchronisierungsvorgang auf dem angegebenen virtuellen Computer aus.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Resynchronize-Methode der Msvm_ReplicationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 007a2a620c1ce9ba867b86a1a9dd1ac77324b6712ef04b8ad10736e1ceac3624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913970"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a>Resynchronize-Methode der Msvm \_ ReplicationService-Klasse

Führt einen Neusynchronisierungsvorgang auf dem angegebenen virtuellen Computer aus. Wenn ein Client diese Methode für einen virtuellen Replikatcomputer aufruft, wird er mit dem erweiterten Replikat neu synchronisiert.

Diese Methode vergleicht die replikationsfähigen Datenträger auf dem primären und dem virtuellen Wiederherstellungscomputer und behebt alle Probleme mit der Datenintegrität der Replikation, indem die verschiedenen Blöcke vom primären Computer zur Wiederherstellung repliziert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, der erneut synchronisiert werden soll.

</dd> <dt>

*StartTime* \[ In\]
</dt> <dd>

Die geplante Startzeit für den Beginn des Neusynchronisierungsvorgang. Wenn dieser Parameter NULL **ist,** wird der Neusynchronisierungsvorgang sofort gestartet.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

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

**Datei nicht gefunden** (32779)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

