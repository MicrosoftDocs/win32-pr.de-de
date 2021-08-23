---
description: Enthält eine Liste der BSS-Bezeichner (Basic Service Set).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST-Struktur (Windot11.h)
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
ms.openlocfilehash: 8abcd2e711d5598c59bb8d4b7aed0f291364f94d04ec17a5fc80de2fd32939eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801390"
---
# <a name="dot11_bssid_list-structure"></a>DOT11 \_ BSSID \_ LIST-Struktur

Die **DOT11 \_ BSSID \_ LIST-Struktur** enthält eine Liste der BSS-Bezeichner (Basic Service Set).

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

Eine [**NDIS \_ OBJECT \_ HEADER-Struktur,**](ndis-object-header.md) die die Typ-, Versions- und Größeninformationen einer NDIS-Struktur enthält. Legen Sie für die meisten **DOT11 \_ BSSID \_ LIST-Strukturen** den **Type-Member** auf **NDIS \_ OBJECT TYPE \_ \_ DEFAULT** fest, legen Sie den **Revisionsmember** auf **DOT11 \_ BSSID \_ LIST REVISION \_ \_ 1** und den **Size-Member** auf **sizeof(DOT11 \_ BSSID \_ LIST)** fest.

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

Die Anzahl der Einträge in dieser Struktur.

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

Die Gesamtzahl der unterstützten Einträge.

</dd> <dt>

**BSSIDs**
</dt> <dd>

Eine Liste von BSS-Bezeichnern. Ein BSS-Bezeichner wird als [**\_ DOT11 MAC \_ ADDRESS-Typ**](dot11-mac-address-type.md) gespeichert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                       |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Windot11.h (einschließlich Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ \_ WLAN-VERBINDUNGSPARAMETER**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




