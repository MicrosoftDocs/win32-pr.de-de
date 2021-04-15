---
title: ICM_DRAW_SUGGESTFORMAT Meldung (VFW. h)
description: Die ICM \_ Draw- \_ Message-Nachricht fragt einen renderingtreiber ab, um ein dekomprimiertes Format vorzuschlagen, das gezeichnet werden kann.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT-Nachricht (Multimedia)
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
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475702"
---
# <a name="icm_draw_suggestformat-message"></a>ICM \_ Draw-Vorschlags \_ Format Meldung

Die **ICM \_ Draw \_** -Message-Nachricht fragt einen renderingtreiber ab, um ein dekomprimiertes Format vorzuschlagen, das gezeichnet werden kann.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwvorschlagen*
</dt> <dd>

Zeiger auf eine [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) -Struktur.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe (in Bytes) von [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK zurück. Wenn der **lpbisuggest** -Member der [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) -Struktur **null** ist, gibt diese Meldung die Menge an Arbeitsspeicher zurück, die für das vorgeschlagene Format erforderlich ist.

## <a name="remarks"></a>Bemerkungen

Der Treiber sollte das im **lpbiin** -Member der [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) -Struktur angegebene Format untersuchen und den **lpbisuggest** -Member verwenden, um ein Format zurückzugeben, das es zeichnen kann. Das Ausgabeformat sollte so viele Daten wie möglich aus dem Eingabeformat erhalten.

Optional kann der Treiber den installierbaren kompressorhandle verwenden, der im **hicdecompressor** -Member von [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) übergeben wurde, um komplexere Auswahlmöglichkeiten zu treffen. Wenn das Eingabeformat z. b. 24-Bit-JPEG-Daten ist, könnte ein Renderer den Dekompressor Abfragen, um herauszufinden, ob er in ein YUV-Format dekomprimiert werden kann (das möglicherweise effizienter gezeichnet wird), bevor das zu verwendende Format ausgewählt wird.

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

 

 





