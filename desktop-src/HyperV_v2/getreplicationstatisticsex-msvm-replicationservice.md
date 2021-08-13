---
description: Ruft die Replikationsstatistiken ab, die der angegebenen Replikationsbeziehung des virtuellen Computers zugeordnet sind.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: Msvm_ReplicationService::GetReplicationStatisticsEx-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d4386692dcaf86527e28b82c91415bf858b47cd19bbc4693af6bff12255138c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253700"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a>Msvm \_ ReplicationService::GetReplicationStatisticsEx-Methode

Ruft die Replikationsstatistiken ab, die der angegebenen Replikationsbeziehung des virtuellen Computers zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den die Replikationsstatistik abgerufen werden soll.

</dd> <dt>

*ReplicationRelationship* \[ In\]
</dt> <dd>

Eine Zeichenfolgendarstellung einer eingebetteten Instanz der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) die die Replikationsbeziehung definiert, für die die Replikationsstatistiken abgerufen werden sollen.

</dd> <dt>

*ReplicationStatistics* \[ out\]
</dt> <dd>

Bei Erfolg empfängt eine eingebettete Instanz der [**Msvm \_ ReplicationStatistics-Klasse,**](msvm-replicationstatistics.md) die die Replikationsstatistiken für die angeforderte Replikationsbeziehung enthält.

</dd> <dt>

*ReplicationHealthIssues* \[ out\]
</dt> <dd>

Wenn erfolgreich, empfängt ein Array eingebetteter Instanzen der [**Msvm \_ Error-Klasse,**](msvm-error.md) die replikationswarnungen oder -fehler für den angeforderten virtuellen Computer angeben.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85)) Dieser Verweis kann NULL **sein,** wenn die Aufgabe abgeschlossen ist.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

