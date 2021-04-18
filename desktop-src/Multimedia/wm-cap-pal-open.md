---
title: WM_CAP_PAL_OPEN Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL Open" \_ -Nachricht lädt eine neue Palette aus einer Palettendatei und übergibt sie an einen Aufzeichnungs Treiber.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN-Nachricht (Multimedia)
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
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340973"
---
# <a name="wm_cap_pal_open-message"></a>WM- \_ Cap- \_ \_ Öffnungs Nachricht öffnen

Die " **WM \_ Cap \_ PAL \_ Open** "-Nachricht lädt eine neue Palette aus einer Palettendatei und übergibt sie an einen Aufzeichnungs Treiber. Palettendateien verwenden normalerweise die Dateinamenerweiterung. Straf. Ein Aufzeichnungs Treiber verwendet eine Palette, wenn dies für das angegebene digitalisierte Bildformat erforderlich ist. Sie können diese Nachricht explizit oder mithilfe des [**cappaletteopen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) -Makros senden.


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den palettendateinamen enthält.

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

 

 





