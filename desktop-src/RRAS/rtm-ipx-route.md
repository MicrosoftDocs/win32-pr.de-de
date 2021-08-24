---
title: RTM_IPX_ROUTE -Struktur (Rtm.h)
description: Die RTM \_ IPX \_ ROUTE-Struktur enthält Informationen, die eine Route für die IPX-Protokollfamilie beschreiben.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE structure RAS
- PRTM_IPX_ROUTE Strukturzeiger RAS
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
ms.openlocfilehash: 1e3d14de623fe8d0b3a85118b39d764baa00d2ca5930cfe711be21a91057b6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101830"
---
# <a name="rtm_ipx_route-structure"></a>RTM \_ IPX \_ ROUTE-Struktur

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RTM \_ IPX \_ ROUTE-Struktur** enthält Informationen, die eine Route für die IPX-Protokollfamilie beschreiben.

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

**\_RR-Zeitstempel**
</dt> <dd>

Gibt den Zeitpunkt an, zu dem der Routeneintrag erstellt oder zuletzt aktualisiert wurde. Dieser Member wird vom Routingtabellen-Manager festgelegt. Die Zeit wird als FILETIME-Struktur ausgedrückt.

</dd> <dt>

**RR \_ RoutingProtocol**
</dt> <dd>

Gibt das Routingprotokoll an, das die Route hinzugefügt hat.

</dd> <dt>

**\_RR-Schnittstellen-ID**
</dt> <dd>

Gibt die Schnittstelle an, über die die Route erhalten wurde.

</dd> <dt>

**RR \_ ProtocolSpecificData**
</dt> <dd>

Gibt eine [**PROTOKOLLSPEZIFISCHE \_ \_ DATENstruktur an,**](protocol-specific-data.md) die Arbeitsspeicher enthält, der für Routingprotokolle spezifische Daten reserviert ist.

</dd> <dt>

**\_RR-Netzwerk**
</dt> <dd>

Gibt eine [**IPX-NETZWERKstruktur \_ an,**](ipx-network.md) die eine IP-Netzwerkadresse enthält.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Gibt eine [**IPX \_ NEXT HOP \_ \_ ADDRESS-Struktur**](ipx-next-hop-address.md) an, die die Adresse des Routers des nächsten Hops enthält.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Gibt eine [**\_ IPX-SPEZIFISCHE \_ DATENstruktur**](ipx-specific-data.md) an, die spezifische Daten für die IPX-Protokollfamilie enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Member der **RTM \_ IPX \_ ROUTE-Struktur** sind alle **DWORD-ausgerichtet.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Routing Table Manager Version 1 Reference](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version \_ \_ 1-Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_IPX-NETZWERK**](ipx-network.md)
</dt> <dt>

[**\_IPX-ADRESSE \_ DES NÄCHSTEN \_ HOPS**](ipx-next-hop-address.md)
</dt> <dt>

[**\_IPX-SPEZIFISCHE \_ DATEN**](ipx-specific-data.md)
</dt> </dl>

 

 





