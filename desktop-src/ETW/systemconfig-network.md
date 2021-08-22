---
description: Diese Klasse ist die Ereignistypklasse für Netzwerkereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: 6b196e8c1ad5a997642cc48491e9d1a4b5e73bc26db71d5ea5258f7cf162a00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069690"
---
# <a name="systemconfig_network-class"></a>SystemConfig \_ Network-Klasse

Diese Klasse ist die Ereignistypklasse für Netzwerkereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **SystemConfig \_ Network-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ Network-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Die Größe der Hashtabelle, in der TCP-Kontrollblöcke (TCBs) gespeichert werden. TCP speichert Kontrollblöcke in einer Hashtabelle, damit sie sehr schnell gefunden werden können.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Die höchste Portnummer, die TCP zuweisen kann, wenn eine Anwendung einen verfügbaren Benutzerport vom System anfordert. In der Regel werden kurzlebige Ports (kurz verwendete) portnummern 1024 bis 5000 zugeordnet.

Der Wert für die höchste Benutzerportnummer, die TCP zuweisen kann, wird durch eine Registrierungseinstellung gesteuert. Weitere Informationen finden Sie unter [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Die Anzahl der Partitionen in der Tabelle Transport Control Block. Durch partitionieren der Transport Control Block-Tabelle werden Konflikte für den Tabellenzugriff minimiert. Dies ist besonders bei Multiprozessorsystemen nützlich.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Die Zeit, die verstreichen muss, bevor TCP eine geschlossene Verbindung freigeben und die zugehörigen Ressourcen wiederverwenden kann. Dieses Intervall zwischen Abschluss und Freigabe wird als TIME \_ WAIT-Status oder 2MSL-Status bezeichnet. Während dieser Zeit kann die Verbindung für client und server viel kostengünstiger erneut geöffnet werden als das Herstellen einer neuen Verbindung.

Rfc 793, veröffentlicht von der IETF, erfordert, dass TCP eine geschlossene Verbindung für ein Intervall beibehält, das mindestens der doppelten maximalen Segmentlebensdauer (2MSL) des Netzwerks entspricht. Wenn eine Verbindung freigegeben wird, können das Socketpaar und der TCP-Steuerungsblock (TCB) verwendet werden, um eine andere Verbindung zu unterstützen. Standardmäßig ist die MSL als 120 Sekunden definiert, und der Wert dieses Eintrags ist gleich zwei MSLs oder 4 Minuten. Weitere Informationen finden Sie unter [RFC 793](https://tools.ietf.org/html/rfc973).

Wenn Sie den Wert dieses Eintrags mithilfe einer Registrierungseinstellung reduzieren, kann TCP geschlossene Verbindungen schneller freigeben und so mehr Ressourcen für neue Verbindungen bereitstellen. Wenn der Wert jedoch zu niedrig ist, gibt TCP möglicherweise Verbindungsressourcen frei, bevor die Verbindung abgeschlossen ist, sodass der Server zusätzliche Ressourcen verwenden muss, um die Verbindung wiederherzustellen.

Normalerweise gibt TCP keine geschlossenen Verbindungen frei, bis der Wert dieses Eintrags abläuft. TCP kann jedoch Verbindungen freigeben, bevor dieser Wert abläuft, wenn keine TCP-Kontrollblöcke (TCBs) mehr vorliegen. Die Anzahl der vom System erstellten TCBs wird durch eine Registrierungseinstellung gesteuert. Weitere Informationen finden Sie unter [MaxFreeTCBs.](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10))

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
