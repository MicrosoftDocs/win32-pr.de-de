---
title: WM_CAP_PAL_AUTOCREATE Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL \_ AutoCreate"-Meldung fordert an, dass der Erfassungs Treiber Beispiel Video Frames erstellt und automatisch eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des-Makros cappaletteauto senden.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340991"
---
# <a name="wm_cap_pal_autocreate-message"></a>WM \_ Cap \_ PAL \_ AutoCreate-Meldung

Die " **WM \_ Cap \_ PAL \_ AutoCreate** "-Meldung fordert an, dass der Erfassungs Treiber Beispiel Video Frames erstellt und automatisch eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des-Makros [**cappaletteauto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) senden.


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Anzahl der zu Stichproben enden Frames.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*icolors*
</dt> <dd>

Anzahl der Farben in der Palette. Der Maximalwert für diesen Parameter ist 256.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

Die Videosequenz für Stichproben sollte alle gewünschten Farben in der Palette enthalten. Um die beste Palette zu erhalten, müssen Sie möglicherweise die gesamte Sequenz anstelle eines Teils davon abgleichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





