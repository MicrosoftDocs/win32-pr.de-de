---
description: Setzt die Replikations Statistiken für eine virtuelle Maschine zurück und setzt die primäre Replikations Beziehung des virtuellen Computers zusammen.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Resegtreplicationstatistics-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358906"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Remintreplicationstatistics-Methode der MSVM- \_ replicationservice-Klasse

Setzt die Replikations Statistiken für eine virtuelle Maschine zurück und setzt die primäre Replikations Beziehung des virtuellen Computers zusammen.

> [!Note]  
> Ab Windows 8.1 wird empfohlen, die Replikations Statistiken nicht mehr mithilfe von **recationstatistics** zurückzusetzen. Verwenden Sie stattdessen [**rec treplicationstatisticsex**](resetreplicationstatisticsex-msvm-replicationservice.md).

 

## <a name="syntax"></a>Syntax


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die den virtuellen Computer darstellt, für den die Replikations Statistiken zurückgesetzt werden sollen.

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

[**Getreplicationstatistics**](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> </dl>

 

