---
description: Startet die Replikation eines virtuellen Computers.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: StartReplication-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f774192cf5c65f6fff0d9a1a17df51483984b49efd6be437f0348547eed5082c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050490"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>StartReplication-Methode der Msvm \_ ReplicationService-Klasse

Startet die Replikation eines virtuellen Computers. Wenn ein Client diese Methode für einen virtuellen Replikatcomputer aufruft, wird die Replikation mit einem erweiterten Replikat gestartet.

## <a name="syntax"></a>Syntax


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ ComputerSystem-Instanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den die Replikation gestartet werden soll.

</dd> <dt>

*InitialReplicationType* \[ In\]
</dt> <dd>

Der Übertragungstyp, der zum Ausführen der ersten Replikation verwendet werden soll.

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Netzwerkübertragung** (1)


</dt> <dd>

Netzwerkübertragung.

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exportieren** (2)


</dt> <dd>

Export.

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Netzwerkübertragung mit Seeding** (3)


</dt> <dd>

Netzwerkübertragung mit Seeding.

</dd> </dl> </dd> <dt>

*InitialReplicationExportLocation* \[ In\]
</dt> <dd>

Wenn *InitialReplicationType* 2 (Export) ist, enthält dieser Parameter den vollqualifizierten Pfad des Verzeichnisses, in das die erste Replikation exportiert werden soll. Dieser Parameter wird nicht für andere Werte von *InitialReplicationType* verwendet und kann **NULL** sein. Dieses Verzeichnis kann wiederverwendet werden, um die Replikation mehrerer virtueller Computer zu exportieren. Diese Methode platziert jede Replikation virtueller Computer in einem separaten Unterverzeichnis unter diesem Pfad.

</dd> <dt>

*StartTime* \[ In\]
</dt> <dd>

Die geplante Startzeit für die erste Replikation über die Netzwerkverbindung mit dem Wiederherstellungsserver. Dieser Parameter wird ignoriert, wenn *InitialReplicationType* 2 (Export) ist. Wenn dieser Parameter **NULL** ist, wird die erste Replikation sofort gestartet.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

