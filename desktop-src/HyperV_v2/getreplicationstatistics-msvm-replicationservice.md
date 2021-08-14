---
description: Ruft Replikationsstatistiken für einen virtuellen Computer ab und fungiert für die primäre Replikationsbeziehung des virtuellen Computers.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: GetReplicationStatistics-Methode der Msvm_ReplicationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 767ea873b725523e3d430708dc5485d3d24c62e07e5cebac001b020ee996bd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392915"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>GetReplicationStatistics-Methode der Msvm \_ ReplicationService-Klasse

Ruft Replikationsstatistiken für einen virtuellen Computer ab und fungiert für die primäre Replikationsbeziehung des virtuellen Computers.

> [!Note]  
> Ab Windows 8.1 wird empfohlen, **GetReplicationStatistics** nicht mehr zum Abrufen von Replikationsstatistiken zu verwenden. Verwenden Sie stattdessen [**GetReplicationStatisticsEx.**](getreplicationstatisticsex-msvm-replicationservice.md)

 

## <a name="syntax"></a>Syntax


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den die Replikationsstatistiken abgerufen werden.

</dd> <dt>

*ReplicationStatistics* \[ out\]
</dt> <dd>

Bei Erfolg empfängt eine eingebettete Instanz der [**Msvm \_ ReplicationStatistics-Klasse,**](msvm-replicationstatistics.md) die die Replikationsstatistiken für den angeforderten virtuellen Computer enthält.

</dd> <dt>

*ReplicationHealthIssues* \[ out\]
</dt> <dd>

Wenn erfolgreich, empfängt ein Array eingebetteter Instanzen der [**Msvm \_ Error-Klasse,**](msvm-error.md) die replikationswarnungen oder -fehler für den angeforderten virtuellen Computer angeben.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

