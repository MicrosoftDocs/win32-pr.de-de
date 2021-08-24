---
title: PROTOCOL_SPECIFIC_DATA -Struktur (Rtm.h)
description: Die \_ PROTOKOLLSPEZIFISCHE \_ DATENstruktur enthält Arbeitsspeicher, der für Daten reserviert ist, die für ein bestimmtes Routingprotokoll spezifisch sind.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA Ras-Struktur
- PPROTOCOL_SPECIFIC_DATA Strukturzeiger RAS
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe43e17827a4c6308c7bfd4499de60ec9105a9fa525ab5aad0226887d02ae8e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036460"
---
# <a name="protocol_specific_data-structure"></a>PROTOKOLLSPEZIFISCHE \_ \_ DATENstruktur

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **\_ PROTOKOLLSPEZIFISCHE \_ DATENstruktur** enthält Arbeitsspeicher, der für Daten reserviert ist, die für ein bestimmtes Routingprotokoll spezifisch sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**\_PSD-Daten**
</dt> <dd>

Gibt ein Array von **DWORD-Variablen** an. Dieser Arbeitsspeicher ist für Daten reserviert, die für Routingprotokolle spezifisch sind.

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

[Routing Table Manager Version 1 Reference](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_RTM-IP-ROUTE \_**](rtm-ip-route.md)
</dt> <dt>

[**\_RTM-IPX-ROUTE \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





