---
title: MCI_MAKE_TMSF-Makro (mciapi. h)
description: Das MCI \_ make \_ TMSF-Makro erstellt einen Uhrzeitwert im TMAs-Format (gepackt/Minutes/seconds/seconds/Frames) aus den angegebenen Pfaden, Minuten, Sekunden und Rahmen Werten.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338799"
---
# <a name="mci_make_tmsf-macro"></a>MCI \_ make \_ TMSF-Makro

Das **MCI \_ make \_ TMSF** -Makro erstellt einen Uhrzeitwert im TMAs-Format (gepackt/Minutes/seconds/seconds/Frames) aus den angegebenen Pfaden, Minuten, Sekunden und Rahmen Werten.

## <a name="syntax"></a>Syntax


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*spürt* 
</dt> <dd>

Anzahl der Spuren.

</dd> <dt>

*minutes* 
</dt> <dd>

Anzahl der Minuten.

</dd> <dt>

*Sekunden* 
</dt> <dd>

Anzahl der Sekunden.

</dd> <dt>

*SSE* 
</dt> <dd>

Anzahl der Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeit im gepackten TMSF-Format zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.

Das **MCI \_ make \_ TMSF** -Makro wird wie folgt definiert:


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





