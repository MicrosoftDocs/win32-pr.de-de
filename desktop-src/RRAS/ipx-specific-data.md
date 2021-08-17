---
title: IPX_SPECIFIC_DATA-Struktur (Rtm.h)
description: Die \_ IPX-SPEZIFISCHE \_ DATENstruktur enthält IPX-spezifische Daten.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA Struktur von RAS
- PIPX_SPECIFIC_DATA Strukturzeiger RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0367e02dd8b0a46304538a2e5830e101eb9573e6548383fbae617a856df83621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790748"
---
# <a name="ipx_specific_data-structure"></a>\_IPX-SPEZIFISCHE \_ DATENstruktur

\[Diese API wurde durch die Routing Table Manager Version [2-API](about-routing-table-manager-version-2.md) ersetzt und ist nach Windows Server 2003 nicht mehr verfügbar. Anwendungen sollten die Routing Table Manager Version 2-API verwenden.\]

Die **\_ IPX-SPEZIFISCHE \_ DATENstruktur** enthält IPX-spezifische Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**\_FSD-Flags**
</dt> <dd>

Gibt Flags an, die die Route beschreiben. Derzeit ist dieser Member entweder 0 (null) oder der folgende Flagwert.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**IPX \_ GLOBAL \_ CLIENT \_ WAN \_ ROUTE**</dt> </dl> | Gibt an, dass diese Route für das globale Netzwerk gilt, das allen WAN-Clients zugeordnet ist.<br/> |



 

</dd> <dt>

**FSD \_ TickCount**
</dt> <dd>

Gibt die Anzahl der Ticks an, die zum Erreichen des Zielnetzwerks benötigt werden. Andere Routingprotokolle als RIP sollten ihre Metriken in Ticks konvertieren.

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

Gibt die Hopanzahl an, die der Route zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Referenz zu Routingtabellen-Manager, Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_RTM-IPX-ROUTE \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





