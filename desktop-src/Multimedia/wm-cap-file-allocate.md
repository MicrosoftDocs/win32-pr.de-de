---
title: WM_CAP_FILE_ALLOCATE Meldung (VFW. h)
description: Die "WM Cap"-Datei Zuordnungs \_ \_ \_ Nachricht erstellt eine Erfassungs Datei mit einer angegebenen Größe (weist diese vorab zu). Sie können diese Nachricht explizit oder mithilfe des capfilezuc-Makros senden.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475855"
---
# <a name="wm_cap_file_allocate-message"></a>Datei Zuordnungs Nachricht für WM- \_ Cap \_ \_

Die " **WM Cap"- \_ \_ Datei \_** Zuordnungs Nachricht erstellt eine Erfassungs Datei mit einer angegebenen Größe (weist diese vorab zu). Sie können diese Nachricht explizit oder mithilfe des [**capfilezuc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) -Makros senden.


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*
</dt> <dd>

Größe (in Bytes) zum Erstellen der Erfassungs Datei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

Sie können die Leistung des Streamings erheblich verbessern, indem Sie eine Erfassungs Datei, die groß genug zum Speichern eines gesamten Videoclips ist, vorab zuordnen und die Erfassungs Datei vor dem Erfassen des Clips defragmentieren.

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

 

 





