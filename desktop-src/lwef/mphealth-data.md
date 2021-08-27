---
title: MPHEALTH_DATA-Struktur (MpClient.h)
description: Integritätsbenachrichtigungsdaten.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPHEALTH_DATA Strukturzeiger Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: cb04224d38e639d053b8e20370e2b0db0dc15f44cc647e7205911362112e4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976000"
---
# <a name="mphealth_data-structure"></a>MPHEALTH \_ DATA-Struktur

Integritätsbenachrichtigungsdaten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Hier wird der Benachrichtigungstyp angegeben.

</dd> <dt>

**dwNotificationFlag**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





