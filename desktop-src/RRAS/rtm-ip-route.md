---
title: RTM_IP_ROUTE Struktur (RTM. h)
description: Die RTM \_ -IP- \_ Routen Struktur enthält Informationen, die eine Route beschreiben, die der IP-Protokollfamilie gehört.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE Struktur-RAS
- PRTM_IP_ROUTE-Struktur Zeiger RAS
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
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345524"
---
# <a name="rtm_ip_route-structure"></a>RTM \_ -IP- \_ Routen Struktur

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **RTM \_ -IP- \_ Routen** Struktur enthält Informationen, die eine Route beschreiben, die der IP-Protokollfamilie gehört.

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

**RR- \_ Zeitstempel**
</dt> <dd>

Gibt die Uhrzeit an, zu der der Routen Eintrag erstellt oder zuletzt aktualisiert wurde. Dieser Member wird vom Routing Tabellen-Manager festgelegt. Die Zeit wird als FILETIME-Struktur ausgedrückt.

</dd> <dt>

**RR \_ routingprotocol**
</dt> <dd>

Gibt das Routing Protokoll an, das die Route hinzugefügt hat.

</dd> <dt>

**RR- \_ interfakeid**
</dt> <dd>

Gibt die Schnittstelle an, über die die Route abgerufen wurde.

</dd> <dt>

**RR \_ protocolspecificdata**
</dt> <dd>

Gibt eine [**Protokoll \_ spezifische \_ Daten**](protocol-specific-data.md) Struktur an, die Arbeitsspeicher enthält, der für Routing Protokoll spezifische Daten reserviert ist.

</dd> <dt>

**RR- \_ Netzwerk**
</dt> <dd>

Gibt eine [**IP- \_ Netzwerk**](ip-network.md) Struktur an, die eine IP-Netzwerkadresse enthält.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Gibt eine [**IP \_ - \_ \_ Adress**](ip-next-hop-address.md) Struktur mit dem nächsten Hop an, die die Adresse des Routers für den nächsten Hop enthält.

</dd> <dt>

**RR \_ familyspecificdata**
</dt> <dd>

Gibt eine [**IP- \_ spezifische \_ Daten**](ip-specific-data.md) Struktur an, die für die IP-Protokollfamilie spezifische Daten enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Mitglieder der **RTM \_ -IP- \_ Routen** Struktur sind alle **DWORD** -Elemente ausgerichtet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für Routing Tabellen-Manager Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routing Tabellen-Manager, Version 1, Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**IP- \_ Netzwerk**](ip-network.md)
</dt> <dt>

[**IP- \_ Adresse des nächsten \_ Hops \_**](ip-next-hop-address.md)
</dt> <dt>

[**IP- \_ spezifische \_ Daten**](ip-specific-data.md)
</dt> </dl>

 

 





