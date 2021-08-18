---
title: MPSAMPLE_DATA -Struktur (MpClient.h)
description: Benachrichtigungsdaten, die an die Rückruffunktion für die Beispielübermittlung übergeben werden.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA struktur Legacy Windows Umgebungsfeatures
- PMPSAMPLE_DATA strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafafd2ff7162dcb50bd5e2ea92cd56ab9f073332238dc0742845f9c48c5a588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747413"
---
# <a name="mpsample_data-structure"></a>MPSAMPLE \_ DATA-Struktur

Benachrichtigungsdaten, die an die Rückruffunktion für die Beispielübermittlung übergeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSampleIndex**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Index des Beispielelements, für das der Übermittlungsstatus gemeldet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





