---
title: ICM_DECOMPRESS_GET_PALETTE Meldung (VFW. h)
description: Die ICM- \_ \_ Dekomprimierung get \_ Palette Message fordert an, dass der Video Dekomprimierung-Treiber die Farbtabelle der Ausgabe BITMAPINFOHEADER-Struktur bereitstellt. Sie können diese Nachricht explizit oder mithilfe des icdecompressgetpalette-Makros senden.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339362"
---
# <a name="icm_decompress_get_palette-message"></a>ICM- \_ Dekomprimierung \_ get- \_ palettennachricht

Die **ICM- \_ Dekomprimierung \_ get \_ Palette** Message fordert an, dass der Video Dekomprimierung-Treiber die Farbtabelle der Ausgabe [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur bereitstellt. Sie können diese Nachricht explizit oder mithilfe des [**icdecompressgetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) -Makros senden.


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur, die das Eingabeformat enthält.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur, die die Farbtabelle enthalten soll. Der für die Farbtabelle reservierte Speicherplatz beträgt immer mindestens 256 Farben. Sie können NULL für diesen Parameter angeben, um nur die Größe der Farbtabelle zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Wenn *lpbioutput* ungleich NULL ist, legt der Treiber den **biclrused** -Member von [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) auf die Anzahl der Farben in der Farbtabelle fest. Der Treiber füllt den **bmicolors** -Member von [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) mit den eigentlichen Farben aus.

Der Treiber sollte diese Nachricht nur dann unterstützen, wenn er eine andere Palette als die im Eingabeformat angegebene Palette verwendet.

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

 

