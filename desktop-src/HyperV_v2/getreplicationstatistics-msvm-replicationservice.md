---
description: Ruft Replikations Statistiken für eine virtuelle Maschine ab und fungiert für die primäre Replikations Beziehung des virtuellen Computers.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Getreplicationstatistics-Methode der Msvm_ReplicationService-Klasse
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
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353111"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Getreplicationstatistics-Methode der MSVM- \_ replicationservice-Klasse

Ruft Replikations Statistiken für eine virtuelle Maschine ab und fungiert für die primäre Replikations Beziehung des virtuellen Computers.

> [!Note]  
> Ab Windows 8.1 wird die Verwendung von **getreplicationstatistics** zum Abrufen von Replikations Statistiken nicht mehr empfohlen. Verwenden Sie stattdessen [**getreplicationstatisticsex**](getreplicationstatisticsex-msvm-replicationservice.md).

 

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

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikations Statistiken abgerufen werden sollen.

</dd> <dt>

*Replicationstatistics* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung empfängt eine eingebettete Instanz der [**MSVM- \_ replicationstatistics**](msvm-replicationstatistics.md) -Klasse, die die Replikations Statistiken für den angeforderten virtuellen Computer enthält.

</dd> <dt>

*Replicationhealthissues* \[ vorgenommen\]
</dt> <dd>

Wenn erfolgreich, wird ein Array von eingebetteten Instanzen der [**MSVM- \_ Fehler**](msvm-error.md) Klasse empfangen, die auf Replikations Warnungen oder Fehler für den angeforderten virtuellen Computer hinweisen.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Reabtreplicationstatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> </dl>

 

