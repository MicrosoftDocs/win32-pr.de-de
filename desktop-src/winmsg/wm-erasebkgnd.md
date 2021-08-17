---
description: Wird gesendet, wenn der Fensterhintergrund gelöscht werden muss (z. B. wenn die Größe eines Fensters geändert wird). Die Nachricht wird gesendet, um einen ungültigen Teil eines Fensters für das Zeichnen vorzubereiten.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: WM_ERASEBKGND Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c74c3b0d1dd2e31e88715d0668f53676759c27cb986b6549fe9e001ab394579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931780"
---
# <a name="wm_erasebkgnd-message"></a>WM \_ ERASEBKGND-Nachricht

Wird gesendet, wenn der Fensterhintergrund gelöscht werden muss (z. B. wenn die Größe eines Fensters geändert wird). Die Nachricht wird gesendet, um einen ungültigen Teil eines Fensters für das Zeichnen vorzubereiten.


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

Eine Anwendung sollte einen Wert ungleich 0 (null) zurückgeben, wenn der Hintergrund gelöscht wird. andernfalls sollte 0 (null) zurückgegeben werden.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) löscht den Hintergrund mithilfe des Klassenhintergrundpinsels, der vom **hbrBackground-Member** der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) angegeben wird. Wenn **hbrBackground** **NULL** ist, sollte die Anwendung die **WM \_ ERASEBKGND-Nachricht** verarbeiten und den Hintergrund löschen.

Eine Anwendung sollte als Reaktion auf **WM \_ ERASEBKGND** einen Wert ungleich 0 zurückgeben, wenn sie die Nachricht verarbeitet und den Hintergrund löscht. Dies bedeutet, dass keine weitere Löschung erforderlich ist. Wenn die Anwendung 0 (null) zurückgibt, bleibt das Fenster für das Löschen markiert. (In der Regel gibt dies an, dass der **fErase-Member** der [**PAINTSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-paintstruct) **TRUE** ist.)

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

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Symbole](../menurc/icons.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
