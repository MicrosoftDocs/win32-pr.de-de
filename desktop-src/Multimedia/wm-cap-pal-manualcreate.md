---
title: WM_CAP_PAL_MANUALCREATE Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL \_ manualcreate"-Meldung fordert an, dass der Erfassungs Treiber manuell Video Frames erstellt und eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des cappalettemanual-Makros senden.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE-Nachricht (Multimedia)
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
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740960"
---
# <a name="wm_cap_pal_manualcreate-message"></a>WM \_ Cap \_ PAL \_ manualcreate-Meldung

Die " **WM \_ Cap \_ PAL \_ manualcreate** "-Meldung fordert an, dass der Erfassungs Treiber manuell Video Frames erstellt und eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des [**cappalettemanual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) -Makros senden.


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*in den Griff*
</dt> <dd>

Palettenhistogrammflag. Legen Sie diesen Parameter für jeden Frame, der zum Erstellen der optimalen Palette gehört, auf **true** fest. Nachdem der letzte Frame erfasst wurde, legen Sie diesen Parameter auf " **false** " fest, um die optimale Palette zu berechnen und an den Erfassungs Treiber zu senden.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*icolors*
</dt> <dd>

Anzahl der Farben in der Palette. Der Maximalwert für diesen Parameter ist 256. Dieser Wert wird nur während der Auflistung des ersten Frames in einer Sequenz verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

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

 

 





