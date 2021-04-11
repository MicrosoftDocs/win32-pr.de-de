---
title: ICM_DECOMPRESS_BEGIN Meldung (VFW. h)
description: Die ICM \_ dekomprimieren \_ Begin-Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des icdecompressbegin-Makros senden.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105435"
---
# <a name="icm_decompress_begin-message"></a>ICM- \_ Dekomprimierungs \_ anfangs Nachricht

Die **ICM \_ dekomprimieren \_ Begin** -Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des [**icdecompressbegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) -Makros senden.


```C++
ICM_DECOMPRESS_BEGIN 
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

Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.

## <a name="remarks"></a>Bemerkungen

Wenn der Treiber diese Nachricht empfängt, sollte er Puffer zuordnen und zeitaufwändige Vorgänge ausführen, damit [**ICM \_**](icm-decompress.md) -Nachrichten effizient verarbeitet werden können.

Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw**](icm-draw.md) -Nachricht.

Die **ICM- \_ Dekomprimierungs \_ Begin** -und [**ICM \_ Decompress \_**](icm-decompress-end.md) -Meldungen werden nicht geschachtelt. Wenn der Treiber **ICM \_ Decompress \_** vor dem Beenden der Dekomprimierung mit **ICM \_ Decompress \_ Beenden** empfängt, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

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

 

