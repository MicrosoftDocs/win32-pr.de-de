---
description: Konfiguriert die IP-Einstellungen der Netzwerkadapter, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: SetFailoverNetworkAdapterSettings-Methode der Msvm_ReplicationService-Klasse
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
ms.openlocfilehash: 744c1b2e56fb50e5a0c16db7d03d7558b1ed69360de98f69a4aac795f9f7db63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147763"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a>SetFailoverNetworkAdapterSettings-Methode der Msvm \_ ReplicationService-Klasse

Konfiguriert die IP-Einstellungen des Netzwerkadapters, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen. Diese Konfigurationsparameter werden nach einem Failovervorgang unmittelbar nach dem Herstellen der Kommunikation mit dem KVP Exchange-Integrationskomponente angewendet, die im Gastbetriebssystem ausgeführt wird.

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

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSysteminstanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, dessen Netzwerkadapter konfiguriert werden sollen.

</dd> <dt>

*NetworkSettings* \[ In\]
</dt> <dd>

Ein Array eingebetteter Instanzen von [**Msvm-FailoverNetworkAdapterSettingData-Objekten. \_**](msvm-failovernetworkadaptersettingdata.md) Jede Instanz beschreibt die Konfigurationsparameter für einen der Netzwerkadapter innerhalb des virtuellen Computers. Die **Eigenschaften IPAddresses** und **DHCPEnabled** müssen für jede Instanz angegeben werden.

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
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InitiateFailover**](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RevertFailover**](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

