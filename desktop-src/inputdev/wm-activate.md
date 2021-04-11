---
title: WM_ACTIVATE Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das aktiviert wird, und das Fenster wird deaktiviert.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Tastatur-und Maus Eingaben für WM_ACTIVATE Nachricht
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103407"
---
# <a name="wm_activate-message"></a>WM- \_ Aktivierungs Nachricht

Wird an das Fenster gesendet, das aktiviert wird, und das Fenster wird deaktiviert. Wenn in den Fenstern dieselbe Eingabe Warteschlange verwendet wird, wird die Nachricht synchron gesendet, zuerst an die Fenster Prozedur des Fensters der obersten Ebene, die deaktiviert wird, und dann an die Fenster Prozedur des Fensters der obersten Ebene, das aktiviert wird. Wenn in den Fenstern verschiedene Eingabe Warteschlangen verwendet werden, wird die Nachricht asynchron gesendet, sodass das Fenster sofort aktiviert wird.


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mit dem nieder wertigen Wort wird angegeben, ob das Fenster aktiviert oder deaktiviert wird. Dieser Parameter kann einen der folgenden Werte annehmen. Das höchst wertige Wort gibt den minimierten Zustand des Fensters an, das aktiviert oder deaktiviert wird. Ein Wert ungleich NULL gibt an, dass das Fenster minimiert wird.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**WA \_ Aktiv**</dt> <dt>1</dt> </dl>                | Wird von einer anderen Methode als einem Mausklick aktiviert (z. b. durch einen aufzurufenden Befehl der [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) -Funktion oder durch Verwendung der Tastaturschnittstelle zum Auswählen des Fensters).<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**WA \_ Clickactive**</dt> <dt>2</dt> </dl> | Aktiviert durch einen Mausklick.<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**WA \_ Inaktiv**</dt> <dt>0</dt> </dl>          | Deaktiviert.<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Fenster, das aktiviert oder deaktiviert wird, abhängig vom Wert des *wParam* -Parameters. Wenn das nieder wertige Wort von *wParam* in der **WA \_ inaktiven** Reihenfolge ist, ist *LPARAM* das Handle für das Fenster, das aktiviert wird. Wenn das nieder wertige Wort von *wParam* auf **WA \_ Active** oder **WA \_ clickactive** festgelegt ist, ist *LPARAM* das Handle für das Fenster, das deaktiviert wird. Dieses Handle kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn das Fenster aktiviert wird und nicht minimiert ist, legt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion den Tastaturfokus auf das Fenster fest. Wenn das Fenster durch einen Mausklick aktiviert wird, wird auch eine WM- [**\_ mouseaktivierungs**](wm-mouseactivate.md) -Meldung empfangen.

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

[**"Fenster"**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**WM- \_ moueinaktivierung**](wm-mouseactivate.md)
</dt> <dt>

[**WM- \_ ncaktivierung**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

