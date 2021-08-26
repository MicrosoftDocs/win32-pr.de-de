---
title: RTM_IP_ROUTE-Struktur (Rtm.h)
description: Die \_ \_ RTM-IP-ROUTE-Struktur enthält Informationen, die eine Route im Besitz der IP-Protokollfamilie beschreiben.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE struktur RAS
- PRTM_IP_ROUTE Strukturzeiger RAS
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd854864dcc61397fa52df7af9419a38ac829a81382be6b6190e4cb3db41d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026730"
---
# <a name="rtm_ip_route-structure"></a>\_RTM-IP-ROUTENstruktur \_

\[Diese API wurde von der Routing Table Manager Version [2-API](about-routing-table-manager-version-2.md) abgelöst und ist nicht mehr als Windows Server 2003 verfügbar. Anwendungen sollten die Routing Table Manager Version 2-API verwenden.\]

Die **\_ RTM-IP-ROUTE-Struktur \_** enthält Informationen, die eine Route im Besitz der IP-Protokollfamilie beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a>Member

<dl> <dt>

**\_RR-Zeitstempel**
</dt> <dd>

Gibt den Zeitpunkt an, zu dem der Routeneintrag erstellt oder zuletzt aktualisiert wurde. Dieses Element wird vom Routingtabellen-Manager festgelegt. Die Zeit wird als FILETIME-Struktur ausgedrückt.

</dd> <dt>

**RR \_ RoutingProtocol**
</dt> <dd>

Gibt das Routingprotokoll an, das die Route hinzugefügt hat.

</dd> <dt>

**RR \_ InterfaceID**
</dt> <dd>

Gibt die Schnittstelle an, über die die Route abgerufen wurde.

</dd> <dt>

**RR \_ ProtocolSpecificData**
</dt> <dd>

Gibt eine [**\_ PROTOKOLLSPEZIFISCHE \_ DATENstruktur**](protocol-specific-data.md) an, die Speicher enthält, der für routingprotokollspezifische Daten reserviert ist.

</dd> <dt>

**\_RR-Netzwerk**
</dt> <dd>

Gibt eine [**\_ IP-NETZWERKstruktur**](ip-network.md) an, die eine IP-Netzwerkadresse enthält.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Gibt eine [**IP-NEXT \_ \_ HOP \_ ADDRESS-Struktur**](ip-next-hop-address.md) an, die die Adresse des Next-Hop-Routers enthält.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Gibt eine [**\_ IP-SPEZIFISCHE \_ DATENstruktur**](ip-specific-data.md) an, die IP-Protokollfamilienspezifische Daten enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Member der **\_ RTM-IP-ROUTE-Struktur \_** sind alle **DWORD-ausgerichtet.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz zu Routingtabellen-Manager, Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_IP-NETZWERK**](ip-network.md)
</dt> <dt>

[**\_IP NEXT HOP ADDRESS \_ (IP-ADRESSE DES NÄCHSTEN HOPS) \_**](ip-next-hop-address.md)
</dt> <dt>

[**\_IP-SPEZIFISCHE \_ DATEN**](ip-specific-data.md)
</dt> </dl>

 

 





