---
description: Erstellt zu Testzwecken ein neues Replikat eines virtuellen Computers mit der angegebenen Momentaufnahme.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: TestReplicaSystem-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d23a97e43dce07d8c0ac0b06f2b488f5966ee63d82f5d92eacac017dc8e05de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870250"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a>TestReplicaSystem-Methode der Msvm \_ ReplicationService-Klasse

Erstellt zu Testzwecken ein neues Replikat eines virtuellen Computers mit der angegebenen Momentaufnahme.

## <a name="syntax"></a>Syntax


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den die Replikation getestet werden soll.

</dd> <dt>

*SnapshotSettingData* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ VirtualSystemSettingData-Instanz,**](/previous-versions//cc136954(v=vs.85)) die die Momentaufnahme darstellt, die zum Erstellen des Testfailoversystems verwendet wurde. Wenn dieser Parameter NULL **ist,** muss das Failover ab dem letzten Zeitpunkt ausgeführt werden.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Wenn ein virtueller Computer erfolgreich definiert wurde, empfängt einen Verweis auf eine Instanz der [**\_ CIM-ComputerSystem-Klasse,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den neu definierten virtuellen Testcomputer darstellt. Wenn dieses System nicht mehr benötigt wird, zerstören Sie es, indem Sie die [**DestroySystem-Methode**](destroysystem-msvm-virtualsystemmanagementservice.md) aufrufen.

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

 

