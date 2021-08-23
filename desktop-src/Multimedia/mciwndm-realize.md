---
title: MCIWNDM_REALIZE (Vfw.h)
description: Die MCIWNDM REALIZE-Nachricht erkennt die Palette, die derzeit vom \_ MCI-Gerät in einem MCIWnd-Fenster verwendet wird. Dieses Makro wird mit der MCIWNDM-NACHRICHT \_ REALIZE definiert. Sie können diese Nachricht explizit oder mithilfe des MCIWndRealize-Makros senden.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fdbee3757e1fd3aada5292b86cc37577ccb718315c5b81140ceb14278c37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012618"
---
# <a name="mciwndm_realize-message"></a>MCIWNDM \_ REALIZE-Nachricht

Die **MCIWNDM \_ REALIZE-Nachricht** erkennt die Palette, die derzeit vom MCI-Gerät in einem MCIWnd-Fenster verwendet wird. Dieses Makro wird mit der **MCIWNDM-NACHRICHT \_ REALIZE** definiert. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndRealize-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) senden.


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Hintergrundflag. Geben **Sie TRUE** für diesen Parameter an, wenn das Fenster eine Hintergrundanwendung ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

**MCIWNDM \_ REALIZE** verwendet die Palette des MCI-Geräts und ruft die [**Funktion RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) auf. Wenn Ihre Anwendung die [**WM \_ PALETTECHANGED-**](/windows/desktop/gdi/wm-palettechanged) und [**WM \_ QUERYNEWPALETTE-Nachrichten**](/windows/desktop/gdi/wm-querynewpalette) explizit verarbeitet, sollten Sie diese Meldung in Ihrer Anwendung anstelle von **RealizePalette verwenden.** Wenn der Text eines dieser Meldungshandler nur **RealizePalette** enthält, wird die Nachricht an das MCIWnd-Fenster weitergeleitet, wodurch die Palette automatisch erkannt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

