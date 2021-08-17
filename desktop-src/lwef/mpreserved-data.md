---
title: MPRESERVED_DATA-Struktur (MpClient.h)
description: Reservierte Benachrichtigungsdaten.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPRESERVED_DATA Strukturzeiger Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747654"
---
# <a name="mpreserved_data-structure"></a>MPRESERVED \_ DATA-Struktur

Reservierte Benachrichtigungsdaten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**cbReservedData**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der reservierten Daten in Bytes.

</dd> <dt>

**pbReservedData**
</dt> <dd>

Typ: **BYTE \***

</dd> <dd>

Zeiger auf reservierte Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





