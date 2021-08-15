---
title: WM_CAP_DRIVER_GET_NAME-Nachricht (Vfw.h)
description: Die MELDUNG WM \_ CAP DRIVER GET NAME gibt den Namen des \_ \_ \_ Erfassungstreibers zurück, der mit dem Erfassungsfenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des Makros capDriverGetName senden.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc44efae992f2967cb069c0866fbb7f9febed51ea73f94853a1b017bc57a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369681"
---
# <a name="wm_cap_driver_get_name-message"></a>MELDUNG "WM \_ CAP \_ DRIVER GET \_ \_ NAME"

Die **MELDUNG WM CAP DRIVER GET \_ \_ \_ \_ NAME** gibt den Namen des Erfassungstreibers zurück, der mit dem Erfassungsfenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) senden.


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe des Puffers in Bytes, auf den von **szName** verwiesen wird.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf einen anwendungsdefinierte Puffer, der verwendet wird, um den Gerätenamen als auf NULL endende Zeichenfolge zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn das Erfassungsfenster nicht mit einem Erfassungstreiber verbunden ist.

## <a name="remarks"></a>Hinweise

Der Name ist eine Textzeichenfolge, die aus dem Ressourcenbereich des Treibers abgerufen wird. Anwendungen sollten für diese Zeichenfolge ungefähr 80 Bytes zuordnen. Wenn der Treiber keine Namensressource enthält, wird der vollständige Pfadname des Treibers zurückgegeben, der in der Registrierung oder in der SYSTEM.INI-Datei aufgeführt ist.

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

 

 





