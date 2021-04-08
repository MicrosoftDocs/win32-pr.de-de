---
title: MCIWNDM_REALIZE Meldung (VFW. h)
description: Die mciwndm- \_ Meldung "erkennen" erkennt die Palette, die zurzeit vom MCI-Gerät in einem mciwnd-Fenster verwendet wird. Dieses Makro wird mit der Meldung "mciwndm-Erkenntnis" definiert \_ . Sie können diese Nachricht explizit oder mithilfe des mciwndrealize-Makros senden.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE-Nachricht (Multimedia)
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
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949483"
---
# <a name="mciwndm_realize-message"></a>Mciwndm-Fehler \_ Meldung

Die **mciwndm \_** -Meldung "erkennen" erkennt die Palette, die zurzeit vom MCI-Gerät in einem mciwnd-Fenster verwendet wird. Dieses Makro wird mit der Meldung " **mciwndm- \_ Erkenntnis** " definiert. Sie können diese Nachricht explizit oder mithilfe des [**mciwndrealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) -Makros senden.


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*"f"*
</dt> <dd>

Hintergrundflag. Geben Sie **true** für diesen Parameter an, wenn das Fenster eine Hintergrund Anwendung ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

**Mciwndm \_ "Erkennen** " verwendet die Palette des MCI-Geräts und ruft die [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) -Funktion auf. Wenn die Anwendung die Nachrichten " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " und " [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) " explizit verarbeitet, sollten Sie diese Meldung in der Anwendung verwenden, anstatt **RealizePalette** zu verwenden. Wenn der Text eines dieser Nachrichten Handler nur **RealizePalette** enthält, leiten Sie die Nachricht an das mciwnd-Fenster weiter, wodurch die Palette automatisch erkannt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndrealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

