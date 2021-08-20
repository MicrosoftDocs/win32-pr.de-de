---
title: MCI_MAKE_TMSF-Makro (Mciapi.h)
description: Das MCI MAKE TMSF-Makro erstellt einen Zeitwert im \_ TMSF-Format (Gepackte Spuren/Minuten/Sekunden/Frames) aus den angegebenen Werten für Spuren, Minuten, Sekunden und \_ Frames.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF-Makros Windows Multimedia
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
ms.openlocfilehash: ec038e0eb1e46c46162c9a2139f03881689db5fe1ee5993a8e135e5d92d67984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138403"
---
# <a name="mci_make_tmsf-macro"></a>MCI \_ MAKE \_ TMSF-Makro

Das **MCI \_ MAKE \_ TMSF-Makro** erstellt einen Zeitwert im TMSF-Format (Gepackte Spuren/Minuten/Sekunden/Frames) aus den angegebenen Werten für Spuren, Minuten, Sekunden und Frames.

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

*Tracks* 
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

*Frames* 
</dt> <dd>

Anzahl von Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Uhrzeit im gepackten TMSF-Format zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im TMSF-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Spuren, dem nächsten am wenigsten signifikanten Byte mit Minuten, dem nächsten am wenigsten signifikanten Byte mit Sekunden und dem wichtigsten Byte mit Frames ausgedrückt.

Das **MCI \_ MAKE \_ TMSF-Makro** ist wie folgt definiert:


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
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





