---
title: WM_CAP_SET_CALLBACK_CAPCONTROL (Vfw.h)
description: Die WM CAP SET CALLBACK CAPCONTROL-Nachricht legt eine Rückruffunktion in der Anwendung fest, die \_ \_ eine präzise \_ \_ Aufzeichnungssteuerung ermöglicht. Sie können diese Nachricht explizit oder mithilfe des Makros capSetCallbackOnCapControl senden.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e5786ef67fe66c7ad0dac463824dcd49bfb34e4c8239ddca74ed60e3861bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369518"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL-Meldung

Die **WM CAP SET \_ \_ \_ CALLBACK \_ CAPCONTROL-Nachricht** legt eine Rückruffunktion in der Anwendung fest, die eine präzise Aufzeichnungssteuerung ermöglicht. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) senden.


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Zeiger auf die Rückruffunktion vom Typ [**capControlCallback.**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback) Geben **Sie NULL** für diesen Parameter an, um eine zuvor installierte Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, oder **FALSE,** wenn eine Streamingerfassungs- oder Singleframe-Erfassungssitzung in Bearbeitung ist.

## <a name="remarks"></a>Hinweise

Eine einzelne Rückruffunktion wird verwendet, um der Anwendung genaue Kontrolle über die Zeiten zu geben, in denen die Streamingerfassung beginnt und abgeschlossen wird. Das Erfassungsfenster ruft zuerst die Prozedur auf, bei der *nState* auf CONTROLCALLBACK PREROLL festgelegt ist, nachdem alle Puffer zugeordnet und alle anderen \_ Erfassungsvorbereitungen abgeschlossen wurden. Dies gibt der Anwendung die Möglichkeit, Videoquellen vorab zu erfassen und von der Rückruffunktion zu dem Zeitpunkt zurückzukehren, zu dem die Aufzeichnung beginnt. Der Rückgabewert **TRUE aus** der Rückruffunktion setzt die Erfassung fort, und der Rückgabewert **FALSE** bricht die Erfassung ab. Nachdem die Erfassung begonnen hat, wird diese Rückruffunktion häufig aufgerufen, und *nState* wird auf CONTROLCALLBACK CAPTURING festgelegt, damit die Anwendung die Erfassung beenden kann, indem \_ FALSE zurückgegeben **wird.**

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

 

 





