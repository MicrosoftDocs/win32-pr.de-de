---
title: MPDETECTION_ORIGIN-Enumeration (mpclient. h)
description: Der Erkennungs Ursprung.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPDETECTION_ORIGIN enumerationszeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338722"
---
# <a name="mpdetection_origin-enumeration"></a>Mperkennungs- \_ Ursprungs Enumeration

Der Erkennungs Ursprung.

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

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**mperkennungs- \_ Ursprung \_ unbekannt**
</dt> <dd>

Die Bedrohung hat den Ursprung unbekannt erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**mperkennungs- \_ Ursprungs \_ lokaler \_ Computer**
</dt> <dd>

Auf dem lokalen Computer wurde eine Bedrohung erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**mperkennungs- \_ Ursprung \_ networkshare**
</dt> <dd>

Bedrohungserkennung auf Netzwerkfreigabe.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**mperkennungs- \_ Ursprungs \_ Internet**
</dt> <dd>

Die Bedrohung wurde im Internet erkannt.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**mperkennungs- \_ Ursprungs \_ Ausgangspunkt**
</dt> <dd>

Bedrohungserkennung für ausgehende Verbindungen.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**mperkennungs- \_ Ursprungs \_ Eingangs**
</dt> <dd>

Die Bedrohung für eine eingehende Verbindung wurde erkannt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





