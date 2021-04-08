---
title: MPCOMPONENT_STATUS Struktur (mpclient. h)
description: Informationen zum Komponenten Status.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCOMPONENT_STATUS Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741024"
---
# <a name="mpcomponent_status-structure"></a>Mpcomponent- \_ Status Struktur

Informationen zum Komponenten Status.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**fenckbar**
</dt> <dd>

Typ: **bool**

</dd> <dd>

Der Status der Komponente.

</dd> <dt>

**HRESULT**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Der Status "erfolgreich" oder "Fehlercode".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





