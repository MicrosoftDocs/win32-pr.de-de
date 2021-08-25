---
description: Wird an eine Anwendung gesendet, wenn ein Fenster aktiviert wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: WM_IME_SETCONTEXT Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fb3e65b47b5d62b1d37ffaee4dfc5927d76485d0c3e5de02662da64215e43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829250"
---
# <a name="wm_ime_setcontext-message"></a>WM \_ IME \_ SETCONTEXT-Nachricht

Wird an eine Anwendung gesendet, wenn ein Fenster aktiviert wird. Ein Fenster empfängt diese Meldung über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

**TRUE,** wenn das Fenster aktiv ist, **andernfalls FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Anzeigeoptionen Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                   | Bedeutung                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt> </dl> | Zeigen Sie das Kompositionsfenster nach Fenster der Benutzeroberfläche an.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ SHOWUIGUIDWINDOW**</dt> </dl>                      | Zeigen Sie das Fenster "Leitfaden" nach Fenster der Benutzeroberfläche an.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ SHOWUISOFTKBD**</dt> </dl>                               | Zeigen Sie die Softtastatur nach Benutzeroberflächenfenster an.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ SHOWUICGABEDATEWINDOW**</dt> </dl>       | Zeigt das Kandidatenfenster von Index 0 nach Benutzeroberflächenfenster an.<br/> |
| <dl> <dt>ISC \_ SHOWUICEIGENEDATEWINDOW << 1</dt> </dl>                                                                                        | Zeigt das Kandidatenfenster von Index 1 nach Fenster der Benutzeroberfläche an.<br/> |
| <dl> <dt>ISC \_ SHOWUICEIGENEDATEWINDOW << 2</dt> </dl>                                                                                        | Zeigt das Kandidatenfenster von Index 2 nach Benutzeroberflächenfenster an.<br/> |
| <dl> <dt>ISC \_ SHOWUICEIGENEDATEWINDOW << 3</dt> </dl>                                                                                        | Zeigt das Kandidatenfenster von Index 3 nach Benutzeroberflächenfenster an.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den von [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)zurückgegebenen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung ein IME-Fenster erstellt hat, sollte sie [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)aufrufen. Andernfalls sollte diese Meldung an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden.

Wenn die Anwendung das Kompositionsfenster zeichnet, muss das Ime-Standardfenster sein Kompositionsfenster nicht anzeigen. In diesem Fall muss die Anwendung den **\_ ISC-Wert SHOWUICOMPOSITIONWINDOW** aus dem *lParam-Parameter* löschen, bevor die Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)übergeben wird. Um ein bestimmtes Benutzeroberflächenfenster anzuzeigen, sollte eine Anwendung den entsprechenden Wert entfernen, damit der IME ihn nicht anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h);</dt> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Nachrichten](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
