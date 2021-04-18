---
title: WM_CAP_PAL_SAVE Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL Save"- \_ Nachricht speichert die aktuelle Palette in einer Palettendatei. Palettendateien verwenden normalerweise die Dateinamenerweiterung. Straf. Sie können diese Nachricht explizit oder mithilfe des-Makros cappalettesave senden.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339988"
---
# <a name="wm_cap_pal_save-message"></a>WM- \_ Cap- \_ Nachricht zum \_ Speichern

Die " **WM \_ Cap \_ PAL \_ Save** "-Nachricht speichert die aktuelle Palette in einer Palettendatei. Palettendateien verwenden normalerweise die Dateinamenerweiterung. Straf. Sie können diese Nachricht explizit oder mithilfe des-Makros [**cappalettesave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) senden.


```C++
WM_CAP_PAL_SAVE 
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

 

 





