---
description: Fordert an, dass der Replikationsstatus des virtuellen Computers in den angegebenen Wert geändert wird, und verhält sich für die primäre Replikationsbeziehung des virtuellen Computers.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: RequestReplicationStateChange-Methode der Msvm_ComputerSystem Klasse
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
ms.openlocfilehash: 568c5016e77baceaadb8176b683d2fd9e1314ab06b907b6d1d3c4e3398a82c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130620"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>RequestReplicationStateChange-Methode der Msvm \_ ComputerSystem-Klasse

Fordert an, dass der Replikationsstatus des virtuellen Computers in den angegebenen Wert geändert wird, und verhält sich für die primäre Replikationsbeziehung des virtuellen Computers. Während der Zustandsänderung wird die **ReplicationState-Eigenschaft** in den Wert des *RequestedState-Parameters* geändert. Diese Methode wird nur für Instanzen der [**Msvm \_ ComputerSystem-Klasse**](msvm-computersystem.md) unterstützt, die einen virtuellen Computer darstellen.

> [!Note]  
> Ab Windows 8.1 wird empfohlen, **RequestReplicationStateChange** nicht mehr zu verwenden, um eine Änderung des Replikationszustands an fordern. Verwenden Sie stattdessen [**RequestReplicationStateChangeEx.**](msvm-requestreplicationstatechangeex-computersystem.md)

 

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

*RequestedState* \[ In\]
</dt> <dd>

Der neue Replikationsstatus. Muss einer der folgenden Werte sein.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Bereit zum Starten der ersten Replikation** (1)


</dt> <dd>

Bereit zum Starten der ersten Replikation.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf den Abschluss der ersten Replikation** (2)


</dt> <dd>

Warten auf den Abschluss der ersten Replikation.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)


</dt> <dd>

Replikation.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Abgeschlossene synchronisierte Replikation** (4)


</dt> <dd>

Die synchronisierte Replikation ist abgeschlossen.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)


</dt> <dd>

Die Replikation wird angehalten.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Erneute Synchronisierung abbrechen** (9)


</dt> <dd>

Abbrechen der Neusynchronisierung.

</dd> </dl> </dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Verweis auf ein [**Msvm \_ ConcreteJob-Objekt,**](msvm-concretejob.md) das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der -Methode zu erhalten.

</dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                | Beschreibung                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolg<br/>                                                                                                          |
| <dl> <dt>**Überprüfte Methodenparameter – Auftrag gestartet**</dt> <dt>4096</dt> </dl> | Der Übergang ist asynchron.<br/>                                                                                  |
| <dl> <dt>**Fehler**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Der Status ist unbekannt**</dt> <dt>32771.</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Der in einem der Parameter angegebene Wert wird nicht unterstützt.<br/>                                                   |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Ungültiger Zustand für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Der im *RequestedState-Parameter angegebene* Wert wird im aktuellen Replikationsmodus oder -zustand nicht unterstützt.<br/> |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Datei nicht gefunden**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

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

[**Msvm \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

 




