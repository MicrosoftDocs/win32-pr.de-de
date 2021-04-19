---
description: Enthält EAPOL-Konfigurationsparameter.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS Struktur (wzcsapi. h)
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
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350290"
---
# <a name="eapol_intf_params-structure"></a>EAPOL \_ INTF-Parameter \_ Struktur

\[**EAPOL \_ INTF \_** -Parameter werden ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

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

Die Version des Aufrufers. Standard ist "0".

</dd> <dt>

**dwReserved2**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**dbewaffnung-Flags**
</dt> <dd>

Nicht verwendet.

</dd> <dt>

**dbewaffnete-Typ**
</dt> <dd>

Der zu verwendende EAP-Erweiterungstyp. Legen Sie auf 0x00000013 für EAP-TLS und 0x00000026 für PEAP fest.

</dd> <dt>

**dwsizeofssid**
</dt> <dd>

Größe des Netzwerk Bezeichners.

</dd> <dt>

**bSSID**
</dt> <dd>

Netzwerk Bezeichner.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Header Datei "wzcsapi. h" ist im Windows SDK nicht verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                       |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




