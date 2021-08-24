---
description: Speichert die wichtigsten Informationen zu einer wlan-Schnittstelle, die vom Drahtloskonfigurationsdienst verwaltet wird.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY -Struktur (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 8d14c65d49d7ed28e2756c2a690cb4a7efa9000417e896a206710bf4365f8cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065150"
---
# <a name="intf_key_entry-structure"></a>INTF \_ KEY \_ ENTRY-Struktur

\[**INTF \_ KEY \_ ENTRY** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [NATIVE WIFI-API,](native-wifi-reference.md)die ähnliche Funktionen bietet. Weitere Informationen finden Sie unter [Informationen zur nativen WLAN-API.](about-the-native-wifi-api.md)\]

In **der INTF \_ KEY \_ ENTRY-Struktur** werden die wichtigsten Informationen zu einer wlan-Schnittstelle gespeichert, die vom Drahtloskonfigurationsdienst verwaltet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**wszGuid**
</dt> <dd>

Ein Zeiger auf die Schnittstellen-GUID, die als Unicode-Zeichenfolge im folgenden Format dargestellt wird: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die *Headerdatei "Wzcsapi.h"* ist im Windows SDK nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                       |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INTFS \_ KEY \_ TABLE**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




