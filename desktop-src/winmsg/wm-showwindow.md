---
description: Wird an ein Fenster gesendet, wenn das Fenster ausgeblendet oder angezeigt wird.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: WM_SHOWWINDOW Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345569"
---
# <a name="wm_showwindow-message"></a>WM- \_ Show Window-Meldung

Wird an ein Fenster gesendet, wenn das Fenster ausgeblendet oder angezeigt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob ein Fenster angezeigt wird. Wenn *wParam* den Wert **true** hat, wird das Fenster angezeigt. Wenn *wParam* den Wert **false** hat, wird das Fenster ausgeblendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Status des Fensters, das angezeigt wird. Wenn *LPARAM* gleich NULL ist, wurde die Nachricht aufgrund eines Aufrufes der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion gesendet. Andernfalls ist *LPARAM* einem der folgenden Werte.



| Wert                                                                                                                                                                                                                         | Bedeutung                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_ Otherunzoom**</dt> <dt>4</dt> </dl>       | Das Fenster wird angezeigt, weil ein maximiertes Fenster wieder hergestellt oder minimiert wurde.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_ Otherzoom**</dt> <dt>2</dt> </dl>             | Das Fenster wird von einem anderen Fenster abgedeckt, das maximiert ist.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_ Abschließende**</dt> <dt>1</dt> </dl> | Das Fenster Besitzer Fenster wird minimiert.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_ Element Opening**</dt> <dt>3</dt> </dl> | Das Fenster Besitzer Fenster wird wieder hergestellt.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Mit der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion wird das Fenster ausgeblendet oder angezeigt, wie in der Meldung angegeben. Wenn ein Fenster während der Erstellung das [**\_ sichtbare WS**](window-styles.md) -Format aufweist, empfängt das Fenster diese Nachricht, nachdem Sie erstellt wurde, aber bevor Sie angezeigt wird. Ein Fenster empfängt diese Meldung auch dann, wenn der Sichtbarkeits Zustand von der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -oder [**showownedpopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) -Funktion geändert wird.

Die **WM- \_ Show Window** -Meldung wird unter den folgenden Umständen nicht gesendet:

-   Wenn ein überlappendes Fenster der obersten Ebene mit der [**WS- \_ Maximierung**](window-styles.md) oder dem **WS- \_ Minimierungs** Stil erstellt wird.
-   Wenn das " **SW \_ shownormal** "-Flag im Aufrufe der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Showownedpopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
