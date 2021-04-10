---
description: Wird an eine Anwendung gesendet, wenn ein Fenster aktiviert wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: WM_IME_SETCONTEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214635"
---
# <a name="wm_ime_setcontext-message"></a>WM \_ IME- \_ SetContext-Meldung

Wird an eine Anwendung gesendet, wenn ein Fenster aktiviert wird. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

**True** , wenn das Fenster aktiv ist, andernfalls **false** .

</dd> <dt>

*lParam* 
</dt> <dd>

Anzeigeoptionen Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                   | Bedeutung                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ showuicompositionwindow**</dt> </dl> | Fenster "Komposition" nach Benutzeroberflächen Fenster anzeigen.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ showuiguidwindow**</dt> </dl>                      | Zeigen Sie das Fenster "Guide" nach Benutzeroberflächen Fenster an.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ showuisoft kbd**</dt> </dl>                               | Zeigt das Fenster "weiche Tastatur nach Benutzeroberfläche" an.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ showuicandidatewindow**</dt> </dl>       | Anzeigen des Kandidaten Fensters von Index 0 nach Fenster der Benutzeroberfläche.<br/> |
| <dl> <dt>ISC \_ showuicandidatewindow << 1</dt> </dl>                                                                                        | Anzeigen des Kandidaten Fensters von Index 1 nach Benutzeroberflächen Fenster.<br/> |
| <dl> <dt>ISC \_ showuicandidatewindow << 2</dt> </dl>                                                                                        | Anzeigen des Kandidaten Fensters von Index 2 nach Benutzeroberflächen Fenster.<br/> |
| <dl> <dt>ISC \_ showuicandidatewindow << 3</dt> </dl>                                                                                        | Anzeigen des Kandidaten Fensters von Index 3 nach Benutzeroberflächen Fenster.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den von [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**immisuimess**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)zurückgegebenen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung ein IME-Fenster erstellt hat, sollte Sie " [**immisuimess Age**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)" aufgerufen werden. Andernfalls sollte diese Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden.

Wenn die Anwendung das Kompositionsfenster zeichnet, muss das Fenster für die Zusammensetzung des standardmäßigen IME-Fensters nicht angezeigt werden. In diesem Fall muss die Anwendung den Wert von **ISC \_ showuicompositionwindow** aus dem *LPARAM* -Parameter löschen, bevor Sie die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**immisuimess**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)übergibt. Wenn Sie ein bestimmtes Fenster für die Benutzeroberfläche anzeigen möchten, sollte eine Anwendung den entsprechenden Wert entfernen, damit Sie vom IME nicht angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                                      |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Meldungen](input-method-manager-messages.md)
</dt> <dt>

[**Immisuimess Age**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
