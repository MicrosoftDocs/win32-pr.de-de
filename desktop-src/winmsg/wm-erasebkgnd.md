---
description: Wird gesendet, wenn der Fenster Hintergrund gelöscht werden muss (z. b. wenn die Größe eines Fensters geändert wird). Die Nachricht wird gesendet, um einen ungültigen Teil eines Fensters zum Zeichnen vorzubereiten.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: WM_ERASEBKGND Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216959"
---
# <a name="wm_erasebkgnd-message"></a>WM \_ erasebkgnd-Meldung

Wird gesendet, wenn der Fenster Hintergrund gelöscht werden muss (z. b. wenn die Größe eines Fensters geändert wird). Die Nachricht wird gesendet, um einen ungültigen Teil eines Fensters zum Zeichnen vorzubereiten.


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte einen Wert ungleich 0 (null) zurückgeben, wenn Sie den Hintergrund löscht. Andernfalls sollte NULL zurückgegeben werden.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion löscht den Hintergrund mithilfe des klassenhintergrund Pinsels, der durch den **hbrbackground** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur angegeben wird. Wenn **hbrbackground** **null** ist, muss die Anwendung die **WM- \_ erasebkgnd** -Nachricht verarbeiten und den Hintergrund löschen.

Eine Anwendung sollte als Antwort auf **WM \_ erasebkgnd** einen Wert ungleich 0 (null) zurückgeben, wenn Sie die Nachricht verarbeitet und den Hintergrund löscht. Dies weist darauf hin, dass kein weiterer Löschvorgang erforderlich ist. Wenn die Anwendung 0 (null) zurückgibt, bleibt das Fenster zum Löschen markiert. (In der Regel bedeutet dies, dass der **ferase** -Member der [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur " **true**" ist.)

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

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Licher**
</dt> <dt>

[Symbole](../menurc/icons.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
