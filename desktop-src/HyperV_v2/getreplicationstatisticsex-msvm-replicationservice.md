---
description: Ruft die Replikations Statistiken ab, die der angegebenen Replikations Beziehung der virtuellen Maschine zugeordnet sind.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Msvm_ReplicationService:: getreplicationstatisticsex-Methode'
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
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356511"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a>MSVM \_ replicationservice:: getreplicationstatisticsex-Methode

Ruft die Replikations Statistiken ab, die der angegebenen Replikations Beziehung der virtuellen Maschine zugeordnet sind.

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

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikations Statistiken abgerufen werden sollen.

</dd> <dt>

*Replicationrelationship* \[ in\]
</dt> <dd>

Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die Replikations Beziehung definiert, für die die Replikations Statistiken abgerufen werden sollen.

</dd> <dt>

*Replicationstatistics* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung empfängt eine eingebettete Instanz der [**MSVM- \_ replicationstatistics**](msvm-replicationstatistics.md) -Klasse, die die Replikations Statistiken für die angeforderte Replikations Beziehung enthält.

</dd> <dt>

*Replicationhealthissues* \[ vorgenommen\]
</dt> <dd>

Wenn erfolgreich, wird ein Array von eingebetteten Instanzen der [**MSVM- \_ Fehler**](msvm-error.md) Klasse empfangen, die auf Replikations Warnungen oder Fehler für den angeforderten virtuellen Computer hinweisen.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird. Dieser Verweis kann **null** sein, wenn der Task beendet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

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

Das **System wird verwendet** (32774).
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
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Stammvirtualisierung \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> <dt>

[**Reinstalltreplicationstatisticsex**](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

