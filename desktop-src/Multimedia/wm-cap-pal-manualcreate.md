---
title: WM_CAP_PAL_MANUALCREATE Nachricht (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ PAL \_ MANUALCREATE fordert an, dass der Aufzeichnungstreiber Videoframes manuell abnimmt und eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des Makros capPaletteManual senden.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8cc313cb6eae8e757d0777642bbc0ab72fe07fcfbf5b530a6479675c8ab3c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781291"
---
# <a name="wm_cap_pal_manualcreate-message"></a>WM \_ CAP \_ PAL \_ MANUALCREATE message

Die **MELDUNG WM CAP PAL \_ \_ \_ MANUALCREATE** fordert an, dass der Aufzeichnungstreiber Videoframes manuell abnimmt und eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des [**Makros capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) senden.


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Paletten-Histogrammflag. Legen Sie diesen Parameter für jeden Frame, der in der Erstellung der optimalen Palette enthalten ist, auf **TRUE** fest. Nachdem der letzte Frame erfasst wurde, legen Sie diesen Parameter auf **FALSE** fest, um die optimale Palette zu berechnen und an den Erfassungstreiber zu senden.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Anzahl der Farben in der Palette. Der Höchstwert für diesen Parameter ist 256. Dieser Wert wird nur während der Auflistung des ersten Frames in einer Sequenz verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR-Meldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





