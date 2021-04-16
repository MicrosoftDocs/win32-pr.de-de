---
title: MPCALLBACK_TYPE-Enumeration (mpclient. h)
description: Mögliche Rückruf Typen.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPCALLBACK_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476122"
---
# <a name="mpcallback_type-enumeration"></a>Mpcallback- \_ Typenumeration

Mögliche Rückruf Typen.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**mpcallback \_ unbekannt**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**mpcallback- \_ Status**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**mpcallback- \_ Bedrohung**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**mpcallback- \_ Scan**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**mpcallback \_ Bereinigen**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**mpcallback- \_ vorab Überprüfung**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**mpcallback- \_ sigupdate**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**mpcallback- \_ Beispiel**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**mpcallback \_ reserviert**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**mpcallback- \_ Konfigurations \_ Benachrichtigung**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**mpcallback- \_ FastPath**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**mpcallback- \_ Produkt \_ Ablauf**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**mpcallback \_ NIS \_ private**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**mpcallback \_ -Integrität**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**mpcallback- \_ EndOf**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**mpcallback- \_ Malware Toast**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**mpcallback- \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





