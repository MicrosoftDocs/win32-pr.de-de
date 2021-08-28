---
description: Eine Anwendung sendet die WM \_ FONTCHANGE-Nachricht an alle Fenster der obersten Ebene im System, nachdem der Pool der Schriftartressourcen geändert wurde.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: WM_FONTCHANGE-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c88edaf2db356fea2b92ce05769360ac9c8664e913ff6e5a05daaf245d1204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399930"
---
# <a name="wm_fontchange-message"></a>WM \_ FONTCHANGE-Meldung

Eine Anwendung sendet die **WM \_ FONTCHANGE-Nachricht** an alle Fenster der obersten Ebene im System, nachdem der Pool der Schriftartressourcen geändert wurde.

Um diese Nachricht zu senden, rufen Sie die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) mit den folgenden Parametern auf.


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Anwendung, die Schriftarten dem System hinzufügt oder entfernt (z. B. mithilfe der [**Funktion AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) oder [**RemoveFontResource),**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) sollte diese Meldung an alle Fenster der obersten Ebene senden.

Um die **WM \_ FONTCHANGE-Nachricht** an alle Fenster der obersten Ebene zu senden, kann eine Anwendung die **SendMessage-Funktion** aufrufen, wobei der *hwnd-Parameter* auf HWND BROADCAST festgelegt \_ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Schriftarten und Text](fonts-and-text.md)
</dt> <dt>

[Schriftart- und Textnachrichten](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
