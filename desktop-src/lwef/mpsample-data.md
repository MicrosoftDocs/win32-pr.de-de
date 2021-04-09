---
title: MPSAMPLE_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten, die an die Rückruffunktion der Beispiel Übermittlung übergeben werden.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSAMPLE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106298"
---
# <a name="mpsample_data-structure"></a>Mpsample- \_ Datenstruktur

Benachrichtigungs Daten, die an die Rückruffunktion der Beispiel Übermittlung übergeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwsampleingedex**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Index des Beispiel Elements, für das der Übermittlungs Status gemeldet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





