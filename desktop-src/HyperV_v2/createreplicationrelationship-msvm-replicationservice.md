---
description: Erstellt eine neue Replikationsbeziehung für einen virtuellen Computer. Wenn ein Client diese Methode für einen virtuellen Replikatcomputer aufruft, wird die Replikationsbeziehung auf den angegebenen Anbieter erweitert.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: CreateReplicationRelationship-Methode der Msvm_ReplicationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d9b61c2339a426314d5c62fe5481b51ba3960c2650ccbdc40b9b9ebd4761cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150083"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>CreateReplicationRelationship-Methode der Msvm \_ ReplicationService-Klasse

Erstellt eine neue Replikationsbeziehung für einen virtuellen Computer. Wenn ein Client diese Methode für einen virtuellen Replikatcomputer aufruft, wird die Replikationsbeziehung auf den angegebenen Anbieter erweitert.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den die Replikation aktiviert werden soll.

</dd> <dt>

*ReplicationSettingData* \[ In\]
</dt> <dd>

Eine Zeichenfolgendarstellung einer Instanz der [**Msvm \_ ReplicationSettingData-Klasse,**](msvm-replicationsettingdata.md) die die Replikationseinstellungen für die neue Replikationsbeziehung definiert, die für den virtuellen Computer erstellt werden soll.

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

## <a name="remarks"></a>Hinweise

**CreateReplicationRelationship verwendet** eine [**Msvm \_ ReplicationSettingData-Instanz**](msvm-replicationsettingdata.md) (FRSD) als Eingabe. Die zugeordnete FRSD für den virtuellen Computer als Host-zu-Host-Anbieter ist die Standardauswahl. Die FRSD-Eingabe wird auf gültige Einstellungen für jede Eigenschaft für den Standardanbieter überprüft. In dieser Tabelle werden die Validierungsunterschiede in Bezug auf den externen Anbieter zusammengefasst.



| Eigenschaft                                             | Externe Anbieter                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | Identisch mit dem Standardanbieter                           |
| AuthenticationType                                   | Wird ignoriert.                                            |
| CertificateThumbPrint                                | Wird ignoriert.                                            |
| RootCertificateThumbPrint (RO)                       | Wird ignoriert.                                            |
| CompressionEnabled                                   | Identisch mit dem Standardanbieter                           |
| BypassProxyServer                                    | Identisch mit dem Standardanbieter                           |
| RecoveryConnectionPoint                              | Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat) |
| RecoveryHostSystem (RO)                              | Wird ignoriert.                                            |
| PrimaryConnectionPoint (RO)                          | Identisch mit dem Standardanbieter                           |
| PrimaryHostSystem (RO)                               | Identisch mit dem Standardanbieter                           |
| RecoveryServerPortNumber                             | Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat) |
| ReplicateHostKvpItems                                | Wird ignoriert.                                            |
| ApplicationConsistentSnapshotInterval                | Identisch mit dem Standardanbieter                           |
| RecoveryHistory                                      | Identisch mit dem Standardanbieter                           |
| IncludedDisks\[\]                                    | Identisch mit dem Standardanbieter                           |
| AutoResynchronizeEnabled                             | Identisch mit dem Standardanbieter                           |
| AutoResynchronizeIntervalStart                       | Identisch mit dem Standardanbieter                           |
| AutoResynchronizeIntervalEnd                         | Identisch mit dem Standardanbieter                           |
| EnableWriteOrderPreservationAcrossDisks (veraltet) | Identisch mit dem Standardanbieter                           |
| ReplicationInterval                                  | Identisch mit dem Standardanbieter                           |



 

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
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

