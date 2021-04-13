---
description: Fordert an, dass der Replikations Status des virtuellen Computers auf den angegebenen Wert geändert wird und die primäre Replikations Beziehung der virtuellen Maschine auftritt.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Requestreplicationstatechange-Methode der Msvm_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528532"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>Requestreplicationstatechange-Methode der MSVM \_ Computersystem-Klasse

Fordert an, dass der Replikations Status des virtuellen Computers auf den angegebenen Wert geändert wird und die primäre Replikations Beziehung der virtuellen Maschine auftritt. Während die Statusänderung ausgeführt wird, wird die Eigenschaft **replicationstate** in den Wert des *requestedstate* -Parameters geändert. Diese Methode wird nur für Instanzen der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse unterstützt, die eine virtuelle Maschine darstellen.

> [!Note]  
> Ab Windows 8.1 wird empfohlen, " **requestreplicationstatechange** " nicht mehr zu verwenden, um die Änderung des Replikations Zustands anzufordern. Verwenden Sie stattdessen [**requestreplicationstatechangeex**](msvm-requestreplicationstatechangeex-computersystem.md).

 

## <a name="syntax"></a>Syntax


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Requestedstate* \[ in\]
</dt> <dd>

Der neue Replikations Status. Muss einer der folgenden Werte sein.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Die erste Replikation kann gestartet** werden (1).


</dt> <dd>

Bereit zum Starten der ersten Replikation.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf Abschluss der ersten Replikation** (2)


</dt> <dd>

Warten auf den Abschluss der ersten Replikation.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)


</dt> <dd>

Replikation.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierungs Replikation beendet** (4)


</dt> <dd>

Synchronisierungs Replikation ist beendet.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)


</dt> <dd>

Unterbrechen der Replikation

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Neusynchronisierung Abbrechen** (9)


</dt> <dd>

Abbrechen der erneuten Synchronisierung.

</dd> </dl> </dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Verweis auf ein [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.

</dd> <dt>

*Timeoutperiod* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolg<br/>                                                                                                          |
| <dl> <dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt> </dl> | Der Übergang erfolgt asynchron.<br/>                                                                                  |
| <dl> <dt></dt> Fehler <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Status ist unbekannt**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Der in einem der Parameter angegebene Wert wird nicht unterstützt.<br/>                                                   |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Der im *requestedstate* -Parameter angegebene Wert wird im aktuellen Replikations Modus oder-Status nicht unterstützt.<br/> |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Datei nicht gefunden**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

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

[**MSVM \_ Computersystem**](msvm-computersystem.md)
</dt> </dl>

 

 




