---
description: Konfiguriert die IP-Einstellungen der Netzwerkadapter, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Setfailovernetworkadaptersettings-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367927"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a>Setfailovernetworkadaptersettings-Methode der MSVM- \_ replicationservice-Klasse

Konfiguriert die IP-Einstellungen des Netzwerkadapters, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen. Diese Konfigurationsparameter werden nach einem Failovervorgang angewendet, unmittelbar nach dem Einrichten der Kommunikation mit der KVP Exchange-Integrations Komponente, die innerhalb des Gast Betriebssystems ausgeführt wird.

## <a name="syntax"></a>Syntax


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, dessen Netzwerkadapter konfiguriert werden sollen.

</dd> <dt>

*Network Settings* \[ in\]
</dt> <dd>

Ein Array von eingebetteten Instanzen von [**MSVM- \_ failovernetworkadaptersettingdata**](msvm-failovernetworkadaptersettingdata.md) -Objekten. Jede Instanz beschreibt die Konfigurationsparameter für einen der Netzwerkadapter innerhalb des virtuellen Computers. Die Eigenschaften " **IPADRESSEN** " und " **dhcpabled** " müssen für jede Instanz angegeben werden.

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

[**Initiatefailover**](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> <dt>

[**Revertfailover**](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

