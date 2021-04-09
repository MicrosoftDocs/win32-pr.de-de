---
title: MPRESOLVED_REASON-Enumeration (mpclient. h)
description: Mögliche Gründe für das Auflösen eines Fehlers bei der Behebung.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPRESOLVED_REASON enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040773"
---
# <a name="mpresolved_reason-enumeration"></a>Mpregelöste \_ reason-Enumeration

Mögliche Gründe für das Auflösen eines Fehlers bei der Behebung.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**mpregelösten \_ Grund \_ unbekannt**
</dt> <dd>

In einem Fehlerzustand.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**mpregelöste \_ Grund für \_ vollständige \_ Überprüfung**
</dt> <dd>

Es wurde eine vollständige Überprüfung durchgeführt.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**mpregelösten \_ Grund Zeitüberschreitung \_ \_**
</dt> <dd>

Genügend Zeit vergangen. Der Standardwert ist eine Woche.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





