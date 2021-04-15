---
title: WM_CAP_FILE_SAVEDIB Meldung (VFW. h)
description: Die \_ savedib-Nachricht der WM-Cap- \_ Datei \_ kopiert den aktuellen Frame in eine DIB-Datei. Sie können diese Nachricht explizit oder mithilfe des capfilesavedib-Makros senden.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479059"
---
# <a name="wm_cap_file_savedib-message"></a>WM- \_ Cap- \_ Datei ( \_ savedib)

Die **\_ \_ \_ savedib** -Nachricht der WM-Cap-Datei kopiert den aktuellen Frame in eine DIB-Datei. Sie können diese Nachricht explizit oder mithilfe des [**capfilesavedib**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) -Makros senden.


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, die den Namen der Ziel-DIB-Datei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

Wenn der Aufzeichnungs Treiber Frames in einem komprimierten Format bereitstellt, versucht dieser Vorgang, den Frame zu dekomprimieren, bevor die Datei geschrieben wird.

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

 

 





