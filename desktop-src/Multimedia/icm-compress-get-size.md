---
title: ICM_COMPRESS_GET_SIZE Meldung (VFW. h)
description: Mit der ICM- \_ \_ \_ Komprimierung Get Size wird angefordert, dass der Video Komprimierungs Treiber die maximale Größe von einem Datenrahmen bei Komprimierung in das angegebene Ausgabeformat bereitstellt. Sie können diese Nachricht explizit oder mithilfe des iccompressgetsize-Makros senden.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956974"
---
# <a name="icm_compress_get_size-message"></a>ICM- \_ Komprimierung \_ get \_ size-Nachricht

Mit der ICM-Komprimierung **\_ \_ get \_ size** wird angefordert, dass der Video Komprimierungs Treiber die maximale Größe von einem Datenrahmen bei Komprimierung in das angegebene Ausgabeformat bereitstellt. Sie können diese Nachricht explizit oder mithilfe des [**iccompressgetsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) -Makros senden.


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die maximale Anzahl von Bytes zurück, die ein einzelner komprimierter Frame belegen kann.

## <a name="remarks"></a>Bemerkungen

Normalerweise senden Anwendungen diese Nachricht, um zu bestimmen, wie groß ein Puffer für den komprimierten Frame ist.

Der Treiber sollte die Größe des größtmöglichen Frames basierend auf den Eingabe-und Ausgabeformaten berechnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

