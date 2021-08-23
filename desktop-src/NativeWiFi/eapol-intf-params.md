---
description: Enthält EAPOL-Konfigurationsparameter.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS-Struktur (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 3359454196735b8100ea40a9b4add2e8e0398c336bf254eb507b0a4e63a86e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685240"
---
# <a name="eapol_intf_params-structure"></a>EAPOL \_ INTF \_ PARAMS-Struktur

\[**EAPOL \_ INTF \_ PARAMS** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [Native Wifi-API](native-wifi-reference.md), die ähnliche Funktionen bereitstellt. Weitere Informationen finden Sie unter [Informationen zur Native Wifi-API.](about-the-native-wifi-api.md)\]

Enthält EAPOL-Konfigurationsparameter.

## <a name="syntax"></a>Syntax


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Version des Aufrufers. Standard ist "0".

</dd> <dt>

**dwReserved2**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**dwEapFlags**
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

**dwEapType**
</dt> <dd>

Der zu verwendende EAP-Erweiterungstyp. Legen Sie für EAP-TLS 0x00000013 und für PEAP 0x00000026 fest.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Größe des Netzwerkbezeichners.

</dd> <dt>

**Bssid**
</dt> <dd>

Netzwerkbezeichner.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Headerdatei wzcsapi.h ist im Windows SDK nicht verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                       |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



 

 




