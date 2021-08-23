---
title: WM_CAP_FILE_SAVEAS (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ FILE \_ SAVEAS kopiert den Inhalt der Erfassungsdatei in eine andere Datei. Sie können diese Nachricht explizit oder mithilfe des Makros capFileSaveAs senden.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a200b8e73d81072961ec4e6aa7c8e1dd989bf2d8c3e0480c75908a8761ee93b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687010"
---
# <a name="wm_cap_file_saveas-message"></a>WM \_ CAP \_ FILE \_ SAVEAS-Meldung

Die **MELDUNG WM CAP FILE \_ \_ \_ SAVEAS** kopiert den Inhalt der Erfassungsdatei in eine andere Datei. Sie können diese Nachricht explizit oder mithilfe des [**Makros capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) senden.


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf die auf NULL beendete Zeichenfolge, die den Namen der Zieldatei enthält, die zum Kopieren der Datei verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

## <a name="remarks"></a>Hinweise

Diese Meldung ändert weder den Namen noch den Inhalt der aktuellen Erfassungsdatei.

Wenn der Kopiervorgang aufgrund eines vollständigen Datenträgerfehlers nicht erfolgreich ist, wird die Zieldatei automatisch gelöscht.

In der Regel ist eine Erfassungsdatei für das größte erwartete Erfassungssegment vorab zugewiesen, und es kann nur ein Teil davon zum Erfassen von Daten verwendet werden. Diese Meldung kopiert nur den Teil der Datei, der die Erfassungsdaten enthält.

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

 

 





