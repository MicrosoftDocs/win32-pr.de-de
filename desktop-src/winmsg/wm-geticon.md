---
description: Wird an ein Fenster gesendet, um ein Handle für das große oder kleine Symbol abzurufen, das einem Fenster zugeordnet ist. Das System zeigt das große Symbol im Dialogfeld ALT+TAB und das kleine Symbol in der Fensterbeschriftung an.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: WM_GETICON Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df8922fa09cf425594a07768f0d7c9ae0ac09222647f181f45331c2b0d47fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587420"
---
# <a name="wm_geticon-message"></a>WM \_ GETICON-Nachricht

Wird an ein Fenster gesendet, um ein Handle für das große oder kleine Symbol abzurufen, das einem Fenster zugeordnet ist. Das System zeigt das große Symbol im Dialogfeld ALT+TAB und das kleine Symbol in der Fensterbeschriftung an.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des symbols, das abgerufen wird. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                          | Bedeutung                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**SYMBOL \_ BIG**</dt> <dt>1</dt> </dl>          | Rufen Sie das große Symbol für das Fenster ab.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**SYMBOL \_ SMALL**</dt> <dt>0</dt> </dl>    | Rufen Sie das kleine Symbol für das Fenster ab.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**SYMBOL \_ SMALL2**</dt> <dt>2</dt> </dl> | Ruft das kleine Symbol ab, das von der Anwendung bereitgestellt wird. Wenn die Anwendung keines bereitstellt, verwendet das System das vom System generierte Symbol für dieses Fenster.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Der DPI des symbols, das abgerufen wird. Dies kann verwendet werden, um je nach Symbolgröße unterschiedliche Symbole bereitzustellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HICON**

Der Rückgabewert ist ein Handle für das große oder kleine Symbol, abhängig vom Wert von *wParam.* Wenn eine Anwendung diese Nachricht empfängt, kann sie ein Handle an ein großes oder kleines Symbol zurückgeben oder die Nachricht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung diese Nachricht empfängt, kann sie ein Handle an ein großes oder kleines Symbol zurückgeben oder die Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt abhängig vom Wert von *wParam* ein Handle für das große oder kleine Symbol zurück, das dem Fenster zugeordnet ist.

Ein Fenster, für das kein Symbol explizit festgelegt ist (mit **WM \_ SETICON**), verwendet das Symbol für die registrierte Fensterklasse, und in diesem Fall gibt [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 0 für eine **WM \_ GETICON-Nachricht** zurück. Wenn beim Senden einer **WM \_ GETICON-Nachricht** an ein Fenster 0 zurückgegeben wird, rufen Sie als Nächstes die [**GetClassLongPtr-Funktion**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) für das Fenster auf. Wenn 0 zurückgegeben wird, probieren Sie die [**LoadIcon-Funktion**](/windows/win32/api/winuser/nf-winuser-loadicona) aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ SETICON**](wm-seticon.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
