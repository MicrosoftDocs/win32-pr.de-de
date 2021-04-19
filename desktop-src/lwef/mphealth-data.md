---
title: MPHEALTH_DATA Struktur (mpclient. h)
description: Integritäts Benachrichtigungs Daten.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPHEALTH_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343052"
---
# <a name="mphealth_data-structure"></a>Mphealth- \_ Datenstruktur

Integritäts Benachrichtigungs Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwnotificationtype**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Hier wird der Benachrichtigungstyp angegeben.

</dd> <dt>

**dwnotificationflag**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





