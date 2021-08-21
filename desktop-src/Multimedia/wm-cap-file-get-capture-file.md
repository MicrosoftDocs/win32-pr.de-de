---
title: WM_CAP_FILE_GET_CAPTURE_FILE-Nachricht (Vfw.h)
description: Die MELDUNG WM \_ CAP FILE GET CAPTURE FILE gibt den Namen der \_ \_ \_ \_ aktuellen Erfassungsdatei zurück. Sie können diese Nachricht explizit oder mithilfe des CapFileGetCaptureFile-Makros senden.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462f919458078129f6756782c2fde5322b3cd814c3108cb0ba8ee24e2f54c022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135318"
---
# <a name="wm_cap_file_get_capture_file-message"></a>WM \_ CAP FILE GET CAPTURE \_ \_ \_ \_ FILE-Meldung

Die **MELDUNG WM CAP FILE GET CAPTURE \_ \_ \_ \_ \_ FILE** gibt den Namen der aktuellen Erfassungsdatei zurück. Sie können diese Nachricht explizit oder mithilfe des [**CapFileGetCaptureFile-Makros**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) senden.


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe des anwendungsdefinierten Puffers in Bytes, auf den **szName** verweist.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf einen von der Anwendung definierten Puffer, der verwendet wird, um den Namen der Erfassungsdatei als auf NULL endende Zeichenfolge zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Der Standardname der Erfassungsdatei ist C: \\CAPTURE.AVI.

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

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





