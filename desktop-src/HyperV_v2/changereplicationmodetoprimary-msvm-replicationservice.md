---
description: Ändert die erweiterte Replikationsbeziehung in die primäre Beziehung für einen virtuellen Replikatcomputer. Der virtuelle Replikatcomputer muss sich in einem Failoverstatus befinden, für den ein Commit ausgeführt wurde.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: Msvm_ReplicationService::ChangeReplicationModeToPrimary-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 943e8220df0a3be48daf4d21e8d913946c72901c769a031486fc2a7dc38ef74a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042020"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a>Msvm \_ ReplicationService::ChangeReplicationModeToPrimary-Methode

Ändert die erweiterte Replikationsbeziehung in die primäre Beziehung für einen virtuellen Replikatcomputer. Der virtuelle Replikatcomputer muss sich in einem Failoverstatus befinden, für den ein Commit ausgeführt wurde.

## <a name="syntax"></a>Syntax


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ ComputerSystem-Instanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den diese Methode die erweiterte Replikationsbeziehung in die primäre Beziehung ändert.

</dd> <dt>

*ReplicationRelationship* \[ In\]
</dt> <dd>

Eine Zeichenfolgendarstellung einer eingebetteten Instanz der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) die die erweiterte Replikationsbeziehung definiert, die diese Methode in die primäre Beziehung ändert.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde. Dieser Verweis kann **NULL** sein, wenn der Task abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

**Ungültiger Parameter** (32773)
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

