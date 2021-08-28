---
title: WM_CAP_FILE_SET_CAPTURE_FILE (Vfw.h)
description: Die WM \_ CAP FILE SET CAPTURE \_ \_ \_ \_ FILE-Meldung benennt die Datei, die für die Videoaufnahme verwendet wird. Sie können diese Nachricht explizit oder mithilfe des Makros capFileSetCaptureFile senden.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9435a7f0790c8ffe88f6b7ea6228bb2f442b23f5dcb15e2722e59b75c671588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687020"
---
# <a name="wm_cap_file_set_capture_file-message"></a>WM \_ CAP FILE SET CAPTURE \_ \_ \_ \_ FILE-Meldung

Die **WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE-Meldung** benennt die Datei, die für die Videoaufnahme verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**Makros capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) senden.


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf die auf NULL beendete Zeichenfolge, die den Namen der zu verwendenden Erfassungsdatei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **oder FALSE,** wenn der Dateiname ungültig ist, oder wenn streaming- oder single-frame-Erfassung in Bearbeitung ist.

## <a name="remarks"></a>Hinweise

In dieser Meldung wird der Dateiname in einer internen Struktur gespeichert. Die angegebene Datei wird nicht erstellt, reserviert oder geöffnet. Der Standardname der Erfassungsdatei ist C: \\CAPTURE.AVI.

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

 

 





