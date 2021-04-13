---
description: Startet die Replikation eines virtuellen Computers.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Startreplikation-Methode der Msvm_ReplicationService-Klasse
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
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343159"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>Startreplikation-Methode der MSVM- \_ replicationservice-Klasse

Startet die Replikation eines virtuellen Computers. Wenn von einem Client diese Methode für einen virtuellen Replikat Computer aufgerufen wird, wird die Replikation mit dem erweiterten Replikat gestartet.

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

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikation gestartet werden soll.

</dd> <dt>

*Initialreplicationtype* \[ in\]
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

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded-Netzwerkübertragung** (3)


</dt> <dd>

Seeded-Netzwerkübertragung.

</dd> </dl> </dd> <dt>

*Initialreplicationexportlocation* \[ in\]
</dt> <dd>

Wenn *initialreplicationtype* 2 (Export) ist, enthält dieser Parameter den voll qualifizierten Pfad des Verzeichnisses, in das die erste Replikation exportiert werden soll. Dieser Parameter wird nicht für andere Werte von *initialreplicationtype* verwendet und kann **null** sein. Dieses Verzeichnis kann wieder verwendet werden, um die Replikation mehrerer virtueller Computer zu exportieren. Diese Methode platziert die Replikation der virtuellen Computer in einem separaten Unterverzeichnis unter diesem Pfad.

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Die geplante Startzeit für die erste Replikation über die Netzwerkverbindung mit dem Wiederherstellungs Server. Dieser Parameter wird ignoriert, wenn " *initialreplicationtype* " den Wert "2 (Export)" hat. Wenn dieser Parameter **null** ist, wird die erste Replikation sofort gestartet.

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

**System wird verwendet** (32774)
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

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> </dl>

 

