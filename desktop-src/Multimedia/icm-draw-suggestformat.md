---
title: ICM_DRAW_SUGGESTFORMAT (Vfw.h)
description: Die ICM DRAW SUGGESTFORMAT-Nachricht fragt einen Renderingtreiber ab, um ein \_ dekomprimiertes Format zu vorschlagen, \_ das ge zeichnen werden kann.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT von Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 843dd2d398f5be6476a148922f3244113e94ab3fe3c10bac9ee08caefb8c4828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495950"
---
# <a name="icm_draw_suggestformat-message"></a>\_ICM DRAW \_ SUGGESTFORMAT-Nachricht

Die **ICM \_ DRAW \_ SUGGESTFORMAT-Nachricht** fragt einen Renderingtreiber ab, um ein dekomprimiertes Format zu vorschlagen, das ge zeichnen werden kann.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Zeiger auf eine [**ICDRAWSUGGEST-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe von [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich. Wenn der **lpbiSuggest-Member** der [**ICDRAWSUGGEST-Struktur**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) **NULL ist,** gibt diese Meldung die Menge an Arbeitsspeicher zurück, die erforderlich ist, um das vorgeschlagene Format zu enthalten.

## <a name="remarks"></a>Hinweise

Der Treiber sollte das im **lpbiIn-Member** der [**ICDRAWSUGGEST-Struktur**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) angegebene Format untersuchen und das **lpbiSuggest-Member** verwenden, um ein Format zurückzuerkennen, das er zeichnen kann. Das Ausgabeformat sollte so viele Daten wie möglich aus dem Eingabeformat beibehalten.

Optional kann der Treiber das installierbare Strichhandles verwenden, das im **hicDecompressor-Member** von [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) übergeben wird, um komplexere Auswahlen zu treffen. Wenn das Eingabeformat beispielsweise 24-Bit-JPEG-Daten ist, kann ein Renderer den Dekomprimator abfragen, um herauszufinden, ob er in ein YUV-Format dekomprimieren kann (das möglicherweise effizienter gezeichnet wird), bevor er das format vorwählt, das sie vorschlagen möchten.

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

 

 





