---
description: Initiiert das Failback für einen virtuellen Wiederherstellungscomputer.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: Msvm_ReplicationService::InitiateFailback-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b573cf1a0347e8df55b239451d9b99f3d416ebd5b3d0d61e662b6023f07a5b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644946"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a>Msvm \_ ReplicationService::InitiateFailback-Methode

Initiiert das Failback für einen virtuellen Wiederherstellungscomputer.

## <a name="syntax"></a>Syntax


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ ComputerSystem-Instanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den ein Failback initiiert werden soll.

</dd> <dt>

*ReplicationSettingData* \[ In\]
</dt> <dd>

Eine Zeichenfolgendarstellung einer eingebetteten Instanz der [**Msvm \_ ReplicationSettingData-Klasse,**](msvm-replicationsettingdata.md) die die Replikationseinstellungen für das Failback definiert.

</dd> <dt>

*RecoveryPointIdentifier* \[ In\]
</dt> <dd>

Optionale Eingabe, die den Wiederherstellungspunkt identifiziert, an den ein Failback angefordert wird.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde. Dieser Verweis kann verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der -Methode abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

**Ungültiger Parameter** (32773)
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

## <a name="remarks"></a>Hinweise

**InitiateFailback** funktioniert auf einem virtuellen Wiederherstellungscomputer und setzt den virtuellen Computer in den Zustand *WaitingForFailback* um. **InitiateFailback** leitet die Failbackanforderung an den entsprechenden Anbieter weiter, der den Wiederherstellungspunkt von der neuen primären Seite umgekehrt synchronisiert. Nach Abschluss des Failbacks des angeforderten Wiederherstellungspunkts wechselt der Replikationsstatus in den Status *FailbackCompleted.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

