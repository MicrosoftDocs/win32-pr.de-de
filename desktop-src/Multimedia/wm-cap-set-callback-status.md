---
title: WM_CAP_SET_CALLBACK_STATUS Meldung (VFW. h)
description: Die WM-Cap-Richtlinien- \_ \_ \_ Rückruf \_ Statusmeldung legt eine Status Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn der Status des Aufzeichnungs Fensters geändert wird. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonstatus-Makros senden.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475492"
---
# <a name="wm_cap_set_callback_status-message"></a>WM- \_ Cap- \_ \_ Rückruf \_ Status Meldung festlegen

Die WM-Cap-Richtlinien- **\_ \_ \_ Rückruf \_ Status** Meldung legt eine Status Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn der Status des Aufzeichnungs Fensters geändert wird. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonstatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Ein Zeiger auf die Status Rückruffunktion vom Typ [**capstatuscallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka). Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Status Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Anwendungen können optional eine Status Rückruffunktion festlegen. Wenn diese Einstellung festgelegt ist, ruft avicap diese Prozedur in den folgenden Situationen auf:

-   Eine Aufzeichnungs Sitzung ist abgeschlossen.
-   Ein Aufzeichnungs Treiber hat erfolgreich eine Verbindung mit einem Aufzeichnungs Fenster hergestellt.
-   Eine optimale Palette wird erstellt.
-   Die Anzahl der aufgezeichneten Frames wird gemeldet.

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

 

 





