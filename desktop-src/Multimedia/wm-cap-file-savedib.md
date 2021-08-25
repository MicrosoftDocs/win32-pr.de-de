---
title: WM_CAP_FILE_SAVEDIB (Vfw.h)
description: Die WM \_ CAP \_ FILE \_ SAVEDIB-Meldung kopiert den aktuellen Frame in eine DIB-Datei. Sie können diese Nachricht explizit oder mithilfe des Makros capFileSaveDIB senden.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB-Nachricht Windows Multimedia
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
ms.openlocfilehash: 66d6dd9b8675e1fb8625349afc4b3f86347d71d605407d5c99fbca291ade744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803810"
---
# <a name="wm_cap_file_savedib-message"></a>WM \_ CAP \_ FILE \_ SAVEDIB-Meldung

Die **WM CAP FILE \_ \_ \_ SAVEDIB-Meldung** kopiert den aktuellen Frame in eine DIB-Datei. Sie können diese Nachricht explizit oder mithilfe des [**Makros capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) senden.


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf die auf NULL beendete Zeichenfolge, die den Namen der DIB-Zieldatei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

## <a name="remarks"></a>Hinweise

Wenn der Erfassungstreiber Frames in einem komprimierten Format liefert, versucht dieser Aufruf, den Frame vor dem Schreiben der Datei zu dekomprimieren.

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

 

 





