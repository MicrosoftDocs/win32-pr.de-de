---
title: ICM_DECOMPRESS_BEGIN (Vfw.h)
description: Die ICM DECOMPRESS BEGIN-Nachricht benachrichtigt einen Videodekomprimierungstreiber, um die Dekomprimierung \_ \_ von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des Makros ICDecompressBegin senden.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN-Nachricht Windows Multimedia
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
ms.openlocfilehash: f1d26a0ea99f089d558da639dfad99d4551237b180e595912973e0d22f634f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678350"
---
# <a name="icm_decompress_begin-message"></a>\_ICM DECOMPRESS \_ BEGIN-Nachricht

Die **ICM \_ DECOMPRESS \_ BEGIN-Nachricht** benachrichtigt einen Videodekomprimierungstreiber, um die Dekomprimierung von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des [**Makros ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) senden.


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) die das Eingabeformat enthält.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) die das Ausgabeformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird, andernfalls ICERR \_ BADFORMAT.

## <a name="remarks"></a>Hinweise

Wenn der Treiber diese Nachricht empfängt, sollte er Puffer zuordnen und zeitaufwändige Vorgänge für die effiziente Verarbeitung ICM [**\_ DECOMPRESS-Nachrichten**](icm-decompress.md) erledigen.

Wenn der Treiber Daten direkt auf dem Bildschirm dekomprimieren soll, senden Sie die ICM [**\_ DRAW-Nachricht.**](icm-draw.md)

Die **ICM \_ DECOMPRESS \_ BEGIN-** [**und ICM \_ DECOMPRESS \_ END-Meldungen**](icm-decompress-end.md) werden nicht geschachtelt. Wenn Ihr Treiber ICM **\_ DECOMPRESS \_ BEGIN** empfängt, bevor die Dekomprimierung mit ICM **\_ DECOMPRESS \_ END** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

