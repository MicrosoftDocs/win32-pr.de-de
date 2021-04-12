---
description: Speichert die Schlüsselinformationen zu einer drahtlosen LAN-Schnittstelle, die vom drahtlos Konfigurations Dienst verwaltet wird.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY Struktur (wzcsapi. h)
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
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343898"
---
# <a name="intf_key_entry-structure"></a>INTF- \_ Schlüssel \_ Eintrags Struktur

\[**INTF \_ Der Schlüssel \_ Eintrag** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

In der **INTF- \_ Schlüssel \_ Eintrags** Struktur werden die Schlüsselinformationen zu einer vom drahtlos Konfigurations Dienst verwalteten drahtlosen LAN-Schnittstelle gespeichert.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**wszguid**
</dt> <dd>

Ein Zeiger auf die GUID der Schnittstelle, die als Unicode-Zeichenfolge im folgenden Format dargestellt wird: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei " *wzcsapi. h* " ist im Windows SDK nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                       |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**intfs- \_ Schlüssel \_ Tabelle**](intfs-key-table.md)
</dt> <dt>

[**Wzcenumschlag-Schnittstellen**](wzcenuminterfaces.md)
</dt> </dl>

 

 




