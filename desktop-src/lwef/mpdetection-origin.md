---
title: MPDETECTION_ORIGIN -Enumeration (MpClient.h)
description: Ursprung der Erkennung.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN enumeration Legacy Windows Environment Features
- PMPDETECTION_ORIGIN-Enumerationszeiger Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70b46ed86276ccb3fc3bd4d2b26388d778c102c1c1fa3bb7ced8f1ad64cd0203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092360"
---
# <a name="mpdetection_origin-enumeration"></a>MPDETECTION \_ ORIGIN-Enumeration

Ursprung der Erkennung.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION \_ ORIGIN \_ UNKNOWN**
</dt> <dd>

Bedrohung erkannt Ursprung unbekannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION \_ ORIGIN \_ LOCAL \_ MACHINE**
</dt> <dd>

Bedrohung auf dem lokalen Computer erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ ORIGIN \_ NETWORKSHARE**
</dt> <dd>

Bedrohung auf Netzwerkfreigabe erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION \_ ORIGIN \_ INTERNET**
</dt> <dd>

Bedrohung im Internet erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION \_ ORIGIN \_ OUTBOUND**
</dt> <dd>

Bedrohung bei einer ausgehenden Verbindung erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION \_ ORIGIN \_ INBOUND**
</dt> <dd>

Bedrohung bei einer eingehenden Verbindung erkannt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





