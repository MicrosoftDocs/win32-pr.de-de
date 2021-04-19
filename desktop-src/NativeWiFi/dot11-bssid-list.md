---
description: Enthält eine Liste von Basic-Service Set-Bezeichner (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST-Struktur (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349481"
---
# <a name="dot11_bssid_list-structure"></a>DOT11 \_ BSSID- \_ Listenstruktur

Die **DOT11 \_ BSSID- \_ Listen** Struktur enthält eine Liste von Basic-Service Set-bezeichern (BSS).

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Member

<dl> <dt>

**Header**
</dt> <dd>

Eine [**NDIS- \_ Objekt \_ Header**](ndis-object-header.md) Struktur, die den Typ, die Version und die Größen Informationen einer NDIS-Struktur enthält. Legen Sie für die meisten **DOT11 \_ -BSSID- \_ Listen** Strukturen das **Typelement** auf den **NDIS- \_ \_ Objekttyp \_ default** fest, legen Sie das **Revisions** Element auf **DOT11 \_ BSSID \_ List \_ Revision \_ 1** fest, und legen Sie den **size** -Member auf **sizeof (DOT11 \_ BSSID \_ List)** fest.

</dd> <dt>

**unumamaentries**
</dt> <dd>

Die Anzahl der Einträge in dieser-Struktur.

</dd> <dt>

**utotalnumuf-Einträge**
</dt> <dd>

Die Gesamtanzahl unterstützter Einträge.

</dd> <dt>

**BSSIDs**
</dt> <dd>

Eine Liste von BSS-bezeichgern. Ein BSS-Bezeichner wird als [**DOT11 \_ Mac \_**](dot11-mac-address-type.md) -Adresstyp gespeichert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                       |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Windot11. h (Include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WLAN- \_ Verbindungs \_ Parameter**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




