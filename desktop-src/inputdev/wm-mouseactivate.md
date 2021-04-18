---
title: WM_MOUSEACTIVATE Meldung (Winuser. h)
description: Wird gesendet, wenn sich der Cursor in einem inaktiven Fenster befindet und der Benutzer eine Maustaste drückt. Das übergeordnete Fenster empfängt diese Nachricht nur, wenn das untergeordnete Fenster es an die defwindowproc-Funktion übergibt.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEACTIVATE Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103402"
---
# <a name="wm_mouseactivate-message"></a>WM- \_ moulogaktivierungs Meldung

Wird gesendet, wenn sich der Cursor in einem inaktiven Fenster befindet und der Benutzer eine Maustaste drückt. Das übergeordnete Fenster empfängt diese Nachricht nur, wenn das untergeordnete Fenster es an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das übergeordnete Fenster der obersten Ebene des Fensters, das aktiviert wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt den von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion zurückgegebenen Treffer Testwert als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht an. Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.

Das höchst wertige Wort gibt den Bezeichner der Maus Meldung an, die generiert wurde, als der Benutzer eine Maustaste gedrückt hat. Abhängig vom Rückgabewert wird die Maus Nachricht entweder verworfen oder im Fenster gepostet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt an, ob das Fenster aktiviert werden soll und ob der Bezeichner der Maus Nachricht verworfen werden soll. Es muss sich um einen der folgenden Werte handeln:



| Rückgabecode/-wert                                                                                                                                          | BESCHREIBUNG                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**MA \_**</dt> <dt>1</dt> aktivieren </dl>         | Aktiviert das Fenster, und die Maus Meldung wird nicht verworfen.<br/>         |
| <dl> <dt>**MA \_ Activateandeat**</dt> <dt>2</dt> </dl>   | Aktiviert das Fenster und verwirft die Maus Meldung.<br/>                 |
| <dl> <dt>**MA \_ Noaktivierung**</dt> <dt>3</dt> </dl>       | Das Fenster wird nicht aktiviert, und die Maus Meldung wird nicht verworfen.<br/> |
| <dl> <dt>**MA \_ Noactivateandeat**</dt> <dt>4</dt> </dl> | Aktiviert das Fenster nicht, sondern verwirft die Maus Nachricht.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt die Nachricht an das übergeordnete Fenster eines untergeordneten Fensters, bevor eine Verarbeitung erfolgt. Das übergeordnete Fenster bestimmt, ob das untergeordnete Fenster aktiviert werden soll. Wenn das untergeordnete Fenster aktiviert wird, sollte das übergeordnete Fenster " **MA \_ noaktivierungs** " oder " **MA \_ noactivateandeat** " zurückgeben, um zu verhindern, dass das System die Nachricht weiterverarbeitet.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ nchittest**](wm-nchittest.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

