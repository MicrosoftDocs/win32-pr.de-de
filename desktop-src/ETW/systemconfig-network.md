---
description: Diese Klasse ist die Ereignistyp Klasse für Netzwerkereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977584"
---
# <a name="systemconfig_network-class"></a>SystemConfig- \_ Netzwerk Klasse

Diese Klasse ist die Ereignistyp Klasse für Netzwerkereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a>Member

Die **\_ Netzwerk Klasse "SystemConfig** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig- \_ Netzwerk** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Die Größe der Hash Tabelle, in der die TCP-Steuerungsblöcke (TCBS) gespeichert sind. TCP speichert Kontroll Blöcke in einer Hash Tabelle, sodass Sie Sie schnell finden können.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Die höchste Portnummer, die TCP zuweisen kann, wenn eine Anwendung einen verfügbaren Benutzerport vom System anfordert. Normalerweise werden kurzlebige Ports (die kurz verwendet) den Portnummern 1024 bis 5000 zugeordnet.

Der Wert für die höchste Benutzer Portnummer, die TCP zugewiesen werden kann, wird von einer Registrierungs Einstellung gesteuert. Weitere Informationen finden Sie unter [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**Tcbtablepartitions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Die Anzahl der Partitionen in der Transport Steuerungs Block-Tabelle. Durch die Partitionierung der Transport Steuerungs Block Tabelle werden Konflikte für den Tabellen Zugriff minimiert. Dies ist besonders bei Multiprozessorsystemen von nutzen.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Die Zeitspanne, die ververgehen muss, bevor TCP eine geschlossene Verbindung freigeben und deren Ressourcen wieder verwenden kann. Dieses Intervall zwischen Closure und Release wird als Zeit \_ Wartezeit oder 2MSL-Status bezeichnet. Während dieser Zeit kann die Verbindung auf dem Client und dem Server um kostengünstiger wieder geöffnet werden, als eine neue Verbindung herzustellen.

Die vom IETF veröffentlichte RFC 793 erfordert, dass TCP eine geschlossene Verbindung für ein Intervall beibehält, das mindestens der doppelten Segment Lebensdauer (2MSL) des Netzwerks entspricht. Wenn eine Verbindung freigegeben wird, können das Socketpaar und der TCP-Kontroll Block (TCB) zur Unterstützung einer anderen Verbindung verwendet werden. Standardmäßig ist MSL auf 120 Sekunden festgelegt, und der Wert dieses Eintrags ist gleich 2 MSLs oder 4 Minuten. Weitere Informationen finden Sie unter [RFC 793](https://tools.ietf.org/html/rfc973).

Wenn Sie den Wert dieses Eintrags mithilfe einer Registrierungs Einstellung verringern, kann TCP geschlossene Verbindungen schneller freigeben und damit mehr Ressourcen für neue Verbindungen bereitstellen. Wenn der Wert jedoch zu niedrig ist, gibt TCP möglicherweise Verbindungs Ressourcen frei, bevor die Verbindung hergestellt wird, sodass der Server zusätzliche Ressourcen zum erneuten Herstellen der Verbindung verwenden muss.

Normalerweise gibt TCP keine geschlossenen Verbindungen frei, bis der Wert dieses Eintrags abläuft. TCP kann jedoch Verbindungen freigeben, bevor dieser Wert abläuft, wenn die TCP-Steuerungsblöcke (TCBS) nicht ausgeführt werden. Die Anzahl der vom System erstellten TCBS wird von einer Registrierungs Einstellung gesteuert. Weitere Informationen finden Sie unter [maxfreetcbs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
