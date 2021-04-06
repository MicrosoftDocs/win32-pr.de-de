---
title: ICM_DECOMPRESSEX_BEGIN Meldung (VFW. h)
description: Die ICM \_ decompressex \_ Begin-Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Dekomprimierung von Daten vorzubereiten.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742953"
---
# <a name="icm_decompressex_begin-message"></a>ICM- \_ decompressex- \_ Begin-Meldung

Die **ICM \_ decompressex \_ Begin** -Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Dekomprimierung von Daten vorzubereiten.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Zeiger auf eine [**icdecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur, die die Eingabe-und Ausgabeformate enthält.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)(in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.

## <a name="remarks"></a>Bemerkungen

Wenn der Treiber diese Nachricht empfängt, sollte er Puffer zuordnen und zeitaufwändige Vorgänge ausführen, damit [**ICM- \_ decompressex**](icm-decompressex.md) -Nachrichten effizient verarbeitet werden können.

Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Nachricht.

Die **ICM \_ decompressex \_ Begin** -und [**ICM \_ decompressex- \_ endmeldungen**](icm-decompressex-end.md) werden nicht geschachtelt. Wenn Ihr Treiber **ICM \_ decompressex \_ Begin** empfängt, bevor die Dekomprimierung mit **ICM \_ decompressex \_ End** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

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

 

 





