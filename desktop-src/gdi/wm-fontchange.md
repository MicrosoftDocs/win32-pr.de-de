---
description: Eine Anwendung sendet nach dem \_ Ändern des Pools der Schriftart Ressourcen die WM-fontchange-Nachricht an alle Fenster der obersten Ebene im System.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: WM_FONTCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980288"
---
# <a name="wm_fontchange-message"></a>WM- \_ fontchange-Meldung

Eine Anwendung sendet nach dem Ändern des Pools der Schriftart Ressourcen die **WM- \_ fontchange** -Nachricht an alle Fenster der obersten Ebene im System.

Um diese Nachricht zu senden, wenden Sie die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit den folgenden Parametern an.


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

## <a name="remarks"></a>Bemerkungen

Eine Anwendung, die Schriftarten aus dem System hinzufügt oder entfernt (z. b. mithilfe der [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) -Funktion oder der [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) -Funktion), sollte diese Nachricht an alle Fenster der obersten Ebene senden.

Zum Senden der " **WM \_ fontchange** "-Nachricht an alle Fenster der obersten Ebene kann eine Anwendung die **SendMessage** -Funktion mit dem *HWND* -Parameter aufrufen \_ .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht Überschrift Arten und Text](fonts-and-text.md)
</dt> <dt>

[Schriftart und Text Nachrichten](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**Removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
