---
title: WM_CAP_PAL_OPEN-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ PAL \_ OPEN-Nachricht lädt eine neue Palette aus einer Palettendatei und übergibt sie an einen Erfassungstreiber.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29cb831ca0128b0562d6ee53b8e66309d2e1dbd91803dab13202dc4a6723bfa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800579"
---
# <a name="wm_cap_pal_open-message"></a>WM \_ CAP \_ PAL \_ OPEN-Nachricht

Die **WM CAP PAL \_ \_ \_ OPEN-Nachricht** lädt eine neue Palette aus einer Palettendatei und übergibt sie an einen Erfassungstreiber. Palettendateien verwenden in der Regel die Dateinamenerweiterung . Freund. Ein Erfassungstreiber verwendet eine Palette, wenn dies für das angegebene digitalisierte Bildformat erforderlich ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) senden.


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Palettendateinamen enthält.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





