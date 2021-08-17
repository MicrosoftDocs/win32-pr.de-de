---
title: MPCOMPONENT_STATUS -Struktur (MpClient.h)
description: Komponentenstatusinformationen.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS-Struktur Legacy Windows Umgebungsfeatures
- PMPCOMPONENT_STATUS strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747798"
---
# <a name="mpcomponent_status-structure"></a>MPCOMPONENT \_ STATUS-Struktur

Komponentenstatusinformationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**fEnable**
</dt> <dd>

Typ: **BOOL**

</dd> <dd>

Status für die Komponente.

</dd> <dt>

**Hresult**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Erfolgs- oder Fehlercode, der dem Status zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





