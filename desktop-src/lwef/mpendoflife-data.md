---
title: MPENDOFLIFE_DATA-Struktur (MpClient.h)
description: '\ 0034; Ende der Lebensdauer \ 0034; Benachrichtigungsdaten.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPENDOFLIFE_DATA Strukturzeiger Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532ee5f80e76de49c2c20bb01958e95fc13603b8f4b65666639834c5cad0fa72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476282"
---
# <a name="mpendoflife_data-structure"></a>MPENDOFLIFE \_ DATA-Struktur

Benachrichtigungsdaten zum Ende der Lebensdauer.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ftSignatureExpiry**
</dt> <dd>

Typ: **FILETIME**

</dd> <dd>

Der Zeitpunkt, zu dem die Signatur abläuft.

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

Typ: **FILETIME**

</dd> <dd>

Der Zeitpunkt, zu dem die Plattform abläuft.

</dd> <dt>

**fAdminControlled**
</dt> <dd>

Typ: **BOOL**

</dd> <dd>

True, wenn der Administrator die Richtlinie zum Anzeigen der Benachrichtigung steuert. Wenn diese Einstellung festgelegt ist, weist dies die Benutzeroberfläche an, die EOL-Benachrichtigung nicht anzuzeigen.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Typ: **BOOL**

</dd> <dd>

True, wenn "End of Life" aussteht oder abgelaufen ist. False gibt an, dass Benutzeroberflächen und Clients alle EOL-bezogenen Zustände löschen können.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





