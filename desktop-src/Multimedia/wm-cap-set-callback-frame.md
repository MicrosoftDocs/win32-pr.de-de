---
title: WM_CAP_SET_CALLBACK_FRAME (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ SET \_ CALLBACK FRAME legt eine \_ Vorschaurückruffunktion in der Anwendung fest. AVICap ruft dieses Verfahren auf, wenn das Erfassungsfenster Vorschauframes erfasst. Sie können diese Nachricht explizit oder mithilfe des Makros capSetCallbackOnFrame senden.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85321483639135db31750cacf76cc5f0dc4ad42e96474efa1dc17ac84ba4a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369508"
---
# <a name="wm_cap_set_callback_frame-message"></a>WM \_ CAP \_ SET \_ CALLBACK \_ FRAME-Meldung

Die **MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ FRAME** legt eine Vorschaurückruffunktion in der Anwendung fest. AVICap ruft dieses Verfahren auf, wenn das Erfassungsfenster Vorschauframes erfasst. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) senden.


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Zeiger auf die Vorschaurückruffunktion vom Typ [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Geben **Sie NULL** für diesen Parameter an, um eine zuvor installierte Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **oder FALSE,** wenn streaming capture oder eine Singleframe-Erfassungssitzung in Bearbeitung ist.

## <a name="remarks"></a>Hinweise

Das Erfassungsfenster ruft die Rückruffunktion auf, bevor Vorschauframes angezeigt werden. Dadurch kann eine Anwendung den Frame bei Wunsch ändern. Diese Rückruffunktion wird während der Streamingvideoaufnahme nicht verwendet.

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

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





