---
title: RTM_IPX_ROUTE Struktur (RTM. h)
description: Die RTM- \_ IPX- \_ Routen Struktur enthält Informationen, die eine Route für die IPX-Protokollfamilie beschreiben.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE Struktur-RAS
- PRTM_IPX_ROUTE-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949653"
---
# <a name="rtm_ipx_route-structure"></a>RTM- \_ IPX- \_ Routen Struktur

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **RTM- \_ IPX- \_ Routen** Struktur enthält Informationen, die eine Route für die IPX-Protokollfamilie beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
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

Gibt eine [**Protokoll \_ spezifische \_ Daten**](protocol-specific-data.md) Struktur mit Arbeitsspeicher an, der für die für Routing Protokolle spezifischen Daten reserviert ist.

</dd> <dt>

**RR- \_ Netzwerk**
</dt> <dd>

Gibt eine [**IPX- \_ Netzwerk**](ipx-network.md) Struktur an, die eine IP-Netzwerkadresse enthält.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Gibt eine [**IPX \_ - \_ \_ Adresse für den nächsten Hop**](ipx-next-hop-address.md) an, die die Adresse des Routers für den nächsten Hop enthält.

</dd> <dt>

**RR \_ familyspecificdata**
</dt> <dd>

Gibt eine [**IPX- \_ spezifische \_ Daten**](ipx-specific-data.md) Struktur an, die für die IPX-Protokollfamilie spezifische Daten enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Elemente der **RTM- \_ IPX- \_ Routen** Struktur sind alle **DWORD** -Elemente ausgerichtet.

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

[Routing Tabellen-Manager, Version \_ 1, \_ Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**IPX- \_ Netzwerk**](ipx-network.md)
</dt> <dt>

[**IPX- \_ Adresse für nächsten \_ Hop \_**](ipx-next-hop-address.md)
</dt> <dt>

[**IPX- \_ spezifische \_ Daten**](ipx-specific-data.md)
</dt> </dl>

 

 





