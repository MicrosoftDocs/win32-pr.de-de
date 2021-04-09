---
title: WM_CAP_FILE_GET_CAPTURE_FILE Meldung (VFW. h)
description: Die Meldung "WM- \_ Cap- \_ Datei \_ get \_ Capture \_ file" gibt den Namen der aktuellen Erfassungs Datei zurück. Sie können diese Nachricht explizit oder mithilfe des capfilegetcapturefile-Makros senden.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE-Nachricht (Multimedia)
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
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858701"
---
# <a name="wm_cap_file_get_capture_file-message"></a>WM- \_ Cap- \_ Datei Nachricht zum Erfassen der \_ \_ Erfassungs \_ Datei

Die Meldung " **WM- \_ Cap- \_ Datei \_ get \_ Capture \_ File** " gibt den Namen der aktuellen Erfassungs Datei zurück. Sie können diese Nachricht explizit oder mithilfe des [**capfilegetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) -Makros senden.


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) des Anwendungs definierten Puffers, auf den von **szName** verwiesen wird.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ein Zeiger auf einen Anwendungs definierten Puffer, der verwendet wird, um den Namen der Erfassungs Datei als NULL-terminierte Zeichenfolge zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der Standard Dateiname für die Aufzeichnung ist C: \\CAPTURE.AVI.

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

 

 





