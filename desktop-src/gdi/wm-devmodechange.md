---
description: Die WM \_ -devmodechange-Meldung wird immer dann an alle Fenster der obersten Ebene gesendet, wenn der Benutzer die Geräte Modus-Einstellungen ändert.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: WM_DEVMODECHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980289"
---
# <a name="wm_devmodechange-message"></a>WM \_ devmodechange-Meldung

Die **WM- \_ devmodechange** -Meldung wird immer dann an alle Fenster der obersten Ebene gesendet, wenn der Benutzer die Geräte Modus-Einstellungen ändert.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Das Fensterhandle

</dd> <dt>

*Umschlag* 
</dt> <dd>

WM \_ devmodechange

</dd> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Gerätenamen angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht kann nicht direkt an ein Fenster gesendet werden. Um die **WM- \_ devmodechange** -Nachricht an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion mit dem *HWND* -Parameter, der auf HWND-Broadcast festgelegt ist \_ .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Geräte Kontexte](device-contexts.md)
</dt> <dt>

[Gerätekontext Meldungen](device-context-messages.md)
</dt> </dl>

 

 
