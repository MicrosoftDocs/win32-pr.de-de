---
description: Wird an ein Fenster gesendet, um ein Handle für das große oder kleine Symbol abzurufen, das einem Fenster zugeordnet ist. Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: WM_GETICON Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350340"
---
# <a name="wm_geticon-message"></a>WM- \_ GetIcon-Nachricht

Wird an ein Fenster gesendet, um ein Handle für das große oder kleine Symbol abzurufen, das einem Fenster zugeordnet ist. Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des abgerufenen Symbols. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                          | Bedeutung                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Symbol \_ Big**</dt> <dt>1</dt> </dl>          | Rufen Sie das große Symbol für das Fenster ab.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Symbol \_ Kleiner**</dt> <dt>0</dt> </dl>    | Rufen Sie das kleine Symbol für das Fenster ab.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**Symbol \_ SMALL2**</dt> <dt>2</dt> </dl> | Ruft das kleine Symbol ab, das von der Anwendung bereitgestellt wird. Wenn Sie von der Anwendung nicht bereitgestellt wird, verwendet das System das vom systemgenerierte Symbol für dieses Fenster.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Der dpi-für das Symbol, das abgerufen wird. Dies kann verwendet werden, um verschiedene Symbole abhängig von der Symbolgröße bereitzustellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HICON**

Der Rückgabewert ist ein Handle für das große oder kleine Symbol, abhängig vom Wert von *wParam*. Wenn eine Anwendung diese Nachricht empfängt, kann Sie ein Handle an ein großes oder ein kleines Symbol zurückgeben oder die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung diese Nachricht empfängt, kann Sie ein Handle an ein großes oder ein kleines Symbol zurückgeben oder die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt ein Handle für das große oder kleine Symbol zurück, das dem Fenster zugeordnet ist, je nach Wert von *wParam*.

Ein Fenster, für das kein Symbol explizit festgelegt ist (mit **WM \_ SetIcon**), verwendet das Symbol für die registrierte Fenster Klasse, und in diesem Fall gibt [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 0 für eine **WM- \_ GetIcon** -Nachricht zurück. Wenn das Senden einer **WM- \_ GetIcon** -Nachricht an ein Fenster 0 zurückgibt, rufen Sie als nächstes die [**getclasslongptr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) -Funktion für das Fenster auf. Wenn der Wert 0 zurückgibt, versuchen Sie es mit der [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) -Funktion.

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

[**WM \_ -Ziel**](wm-seticon.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
