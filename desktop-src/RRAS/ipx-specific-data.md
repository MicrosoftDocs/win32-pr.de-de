---
title: IPX_SPECIFIC_DATA Struktur (RTM. h)
description: Die IPX \_ \_ -spezifische Datenstruktur enthält IPX-spezifische Daten.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA Struktur-RAS
- PIPX_SPECIFIC_DATA-Struktur Zeiger RAS
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
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949387"
---
# <a name="ipx_specific_data-structure"></a>IPX- \_ spezifische \_ Datenstruktur

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **IPX- \_ spezifische \_ Daten** Struktur enthält IPX-spezifische Daten.

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

**F- \_ Flags**
</dt> <dd>

Gibt Flags an, die die Route beschreiben. Derzeit ist dieser Member entweder NULL oder der folgende Flagwert.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**globale IPX- \_ \_ Client-WAN- \_ \_ Route**</dt> </dl> | Gibt an, dass diese Route für das globale Netzwerk bestimmt ist, das allen WAN-Clients zugeordnet ist.<br/> |



 

</dd> <dt>

**Anzahl der Aktivier- \_ Tickanzahl**
</dt> <dd>

Gibt die Anzahl der Ticks an, die zum Erreichen des Ziel Netzwerks benötigt werden. Bei anderen Routing Protokollen als RIP sollten ihre Metriken in Ticks konvertiert werden.

</dd> <dt>

**Anzahl von "f SD" \_**
</dt> <dd>

Gibt die Hopanzahl an, die der Route zugeordnet ist.

</dd> </dl>

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

[**RTM- \_ IPX- \_ Route**](rtm-ipx-route.md)
</dt> </dl>

 

 





