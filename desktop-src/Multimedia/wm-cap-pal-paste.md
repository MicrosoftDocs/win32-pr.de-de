---
title: WM_CAP_PAL_PASTE (Vfw.h)
description: Die WM \_ CAP \_ PAL \_ PASTE-Meldung kopiert die Palette aus der Zwischenablage und übergibt sie an einen Erfassungstreiber. Sie können diese Nachricht explizit oder mithilfe des Makros capPalettePaste senden.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bedb760a444abe9b0667592855d701dc24a02b8ee57ea15ab30912a5e216d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686830"
---
# <a name="wm_cap_pal_paste-message"></a>WM CAP PAL PASTE message (WM \_ CAP \_ \_ PAL-PASTE-Meldung)

Die **WM CAP PAL \_ \_ \_ PASTE-Meldung** kopiert die Palette aus der Zwischenablage und übergibt sie an einen Erfassungstreiber. Sie können diese Nachricht explizit oder mithilfe des [**Makros capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) senden.


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

## <a name="remarks"></a>Hinweise

Ein Erfassungstreiber verwendet eine Palette, wenn dies für das angegebene formatierte Video erforderlich ist.

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

 

 





