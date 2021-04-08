---
title: WM_CAP_FILE_SET_CAPTURE_FILE Meldung (VFW. h)
description: Die Datei Satz-Erfassungs Datei für die WM-Abdeckung gibt \_ \_ \_ \_ \_ die für die Video Erfassung verwendete Datei an. Sie können diese Nachricht explizit oder mithilfe des capfilesetcapturefile-Makros senden.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE-Nachricht (Multimedia)
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
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949396"
---
# <a name="wm_cap_file_set_capture_file-message"></a>WM- \_ Cap- \_ Datei Satz- \_ \_ Erfassungs \_ Datei Nachricht

Die **Datei \_ \_ Satz- \_ \_ Erfassungs \_** Datei für die WM-Abdeckung gibt die für die Video Erfassung verwendete Datei an. Sie können diese Nachricht explizit oder mithilfe des [**capfilesetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) -Makros senden.


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die den Namen der zu verwendenden Erfassungs Datei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn der Dateiname ungültig ist, oder wenn ein Streaming oder eine einzelne Frame-Erfassung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

In dieser Meldung wird der Dateiname in einer internen Struktur gespeichert. Die angegebene Datei wird nicht erstellt, neu erstellt oder geöffnet. Der Standard Dateiname für die Aufzeichnung ist C: \\CAPTURE.AVI.

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

 

 





