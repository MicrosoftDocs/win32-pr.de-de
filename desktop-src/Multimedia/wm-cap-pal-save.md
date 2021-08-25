---
title: WM_CAP_PAL_SAVE (Vfw.h)
description: Die MELDUNG WM \_ CAP PAL SAVE speichert die aktuelle Palette in einer \_ \_ Palettendatei. Palettendateien verwenden in der Regel die Dateierweiterung . Freund. Sie können diese Nachricht explizit oder mithilfe des Makros capPaletteSave senden.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff8703eafcc3c612fbde5bac7d15433758aa3d6ee44ab47697ffb25f9324dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891880"
---
# <a name="wm_cap_pal_save-message"></a>WM \_ CAP \_ PAL \_ SAVE-Meldung

Die **MELDUNG WM CAP PAL \_ \_ \_ SAVE** speichert die aktuelle Palette in einer Palettendatei. Palettendateien verwenden in der Regel die Dateierweiterung . Freund. Sie können diese Nachricht explizit oder mithilfe des [**Makros capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) senden.


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Palettendateinamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

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

 

 





