---
title: WM_CAP_GET_STATUS (Vfw.h)
description: Die MELDUNG WM \_ CAP GET STATUS ruft den Status des \_ \_ Erfassungsfensters ab. Sie können diese Nachricht explizit oder mithilfe des Makros capGetStatus senden.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805befc3f83c79b157e040004dcf382dccaf07b240b3b846892b8fb035f826ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135156"
---
# <a name="wm_cap_get_status-message"></a>WM CAP GET STATUS message (WM \_ CAP \_ GET \_ STATUS-Meldung)

Die **MELDUNG WM CAP GET \_ \_ \_ STATUS** ruft den Status des Erfassungsfensters ab. Sie können diese Nachricht explizit oder mithilfe des [**Makros capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) senden.


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe der Struktur in Bytes, auf die von **s verwiesen wird.**

</dd> <dt>

<span id="s"></span><span id="S"></span>*s*
</dt> <dd>

Zeiger auf eine [**CAPSTATUS-Struktur.**](/windows/win32/api/vfw/ns-vfw-capstatus)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, oder **FALSE,** wenn das Erfassungsfenster nicht mit einem Erfassungstreiber verbunden ist.

## <a name="remarks"></a>Hinweise

Die [**CAPSTATUS-Struktur**](/windows/win32/api/vfw/ns-vfw-capstatus) enthält den aktuellen Status des Erfassungsfensters. Da dieser Zustand dynamisch ist und sich als Reaktion auf verschiedene Meldungen ändert, sollte die Anwendung diese Struktur initialisieren, nachdem die [**WM \_ CAP \_ DLG \_ VIDEOFORMAT-Nachricht**](wm-cap-dlg-videoformat.md) gesendet wurde (oder das [**Makro capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) verwendet wird) und wann immer sie Menüelemente aktivieren oder den tatsächlichen Zustand des Fensters bestimmen muss.

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

 

 





