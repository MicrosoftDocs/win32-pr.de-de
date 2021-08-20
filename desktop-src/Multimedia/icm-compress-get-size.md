---
title: ICM_COMPRESS_GET_SIZE (Vfw.h)
description: Die ICM COMPRESS GET SIZE-Meldung fordert an, dass der Videokomprimierungstreiber die maximale Größe eines Frames von Daten anliefert, wenn er in das angegebene \_ \_ \_ Ausgabeformat komprimiert wird. Sie können diese Nachricht explizit oder mithilfe des Makros ICCompressGetSize senden.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE von Windows Multimedia
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
ms.openlocfilehash: 0ac84919b81eda747263877a79e8ce6fe6ab3bdfc50d37e77ce2026288fbe321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988173"
---
# <a name="icm_compress_get_size-message"></a>\_ICM COMPRESS \_ GET \_ SIZE-Nachricht

Die **ICM \_ COMPRESS GET \_ \_ SIZE-Meldung** fordert an, dass der Videokomprimierungstreiber die maximale Größe eines Datenrahmens anliefert, wenn er in das angegebene Ausgabeformat komprimiert wird. Sie können diese Nachricht explizit oder mithilfe des [**Makros ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) senden.


```C++
ICM_COMPRESS_GET_SIZE 
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

Gibt die maximale Anzahl von Bytes zurück, die ein einzelner komprimierter Frame belegen kann.

## <a name="remarks"></a>Hinweise

In der Regel senden Anwendungen diese Nachricht, um zu bestimmen, wie groß ein Puffer für den komprimierten Frame zu reservieren ist.

Der Treiber sollte die Größe des größten möglichen Frames basierend auf den Eingabe- und Ausgabeformaten berechnen.

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

 

