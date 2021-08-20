---
title: WM_CAP_SET_CALLBACK_ERROR (Vfw.h)
description: Die MELDUNG WM CAP SET CALLBACK ERROR legt \_ \_ eine \_ \_ Fehlerrückruffunktion in der Clientanwendung fest. AVICap ruft diese Prozedur auf, wenn Fehler auftreten. Sie können diese Nachricht explizit oder mithilfe des Makros capSetCallbackOnError senden.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b631a66923fc614e1486405b1c8e64f152c0f0dd21c8abec292548c546d17b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135102"
---
# <a name="wm_cap_set_callback_error-message"></a>WM CAP SET CALLBACK ERROR message (WM \_ CAP \_ \_ SET-RÜCKRUFFEHLERmeldung) \_

Die **MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ ERROR** legt eine Fehlerrückruffunktion in der Clientanwendung fest. AVICap ruft diese Prozedur auf, wenn Fehler auftreten. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) senden.


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Zeiger auf die Fehlerrückruffunktion vom Typ [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). Geben **Sie NULL** für diesen Parameter an, um eine zuvor installierte Fehlerrückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **oder FALSE,** wenn streaming capture oder eine Singleframe-Erfassungssitzung in Bearbeitung ist.

## <a name="remarks"></a>Hinweise

Anwendungen können optional eine Fehlerrückruffunktion festlegen. Wenn festgelegt, ruft AVICap die Fehlerprozedur in den folgenden Situationen auf:

-   Der Datenträger ist voll.
-   Ein Erfassungsfenster kann nicht mit einem Erfassungstreiber verbunden werden.
-   Ein Waveform-Audio-Gerät kann nicht geöffnet werden.
-   Die Anzahl der während der Erfassung gelöschten Frames überschreitet den angegebenen Prozentsatz.
-   Die Frames können aufgrund von Unterbrechungsproblemen bei der vertikalen Synchronisierung nicht erfasst werden.

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

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





