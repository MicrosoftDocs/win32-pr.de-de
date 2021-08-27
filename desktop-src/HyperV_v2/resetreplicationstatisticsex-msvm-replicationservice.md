---
description: Setzt Replikationsstatistiken zurück, die der angegebenen Replikationsbeziehung des angegebenen virtuellen Computers zugeordnet sind.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: Msvm_ReplicationService::ResetReplicationStatisticsEx-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 613d35a03d224032a07468c2ed2d830c73c3a899df455cc3e0cd68b335797b3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083070"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a>Msvm \_ ReplicationService::ResetReplicationStatisticsEx-Methode

Setzt Replikationsstatistiken zurück, die der angegebenen Replikationsbeziehung des angegebenen virtuellen Computers zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den replikatfähigen virtuellen Computer darstellt.

</dd> <dt>

*ReplicationRelationship* \[ In\]
</dt> <dd>

Eine Zeichenfolgendarstellung einer eingebetteten Instanz der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) die die Replikationsbeziehung definiert, für die die Replikationsstatistiken zurückgesetzt werden sollen.

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

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

