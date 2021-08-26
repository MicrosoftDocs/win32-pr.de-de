---
description: Wird an ein minimiertes Fenster gesendet.
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: WM_QUERYDRAGICON-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20aac405a247f89a31c49f60a4e421fa171465d399dcb61a436936de5c646362
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055990"
---
# <a name="wm_querydragicon-message"></a>WM \_ QUERYDRAGICON-Meldung

Wird an ein minimiertes Fenster gesendet. Das Fenster wird vom Benutzer gezogen, aber es ist kein Symbol für seine Klasse definiert. Eine Anwendung kann ein Handle an ein Symbol oder einen Cursor zurückgeben. Das System zeigt diesen Cursor oder dieses Symbol an, während der Benutzer das Symbol zieht.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte ein Handle an einen Cursor oder ein Symbol zurückgeben, das vom System angezeigt werden soll, während der Benutzer das Symbol zieht. Der Cursor oder das Symbol muss mit der Auflösung des Anzeigetreibers kompatibel sein. Wenn die Anwendung **NULL** zurückgibt, zeigt das System den Standardcursor an.

## <a name="remarks"></a>Hinweise

Wenn der Benutzer das Symbol eines Fensters ohne Klassensymbol zieht, ersetzt das System das Symbol durch einen Standardcursor. Wenn die Anwendung beim Ziehen einen anderen Cursor anzeigen muss, muss sie ein Handle für den Cursor oder das Symbol zurückgeben, das mit der Auflösung des Anzeigetreibers kompatibel ist. Wenn eine Anwendung ein Handle an einen Farbcursor oder ein Farbsymbol zurückgibt, konvertiert das System den Cursor oder das Symbol in Schwarz-Weiß. Die Anwendung kann die [**LoadCursor-**](/windows/win32/api/winuser/nf-winuser-loadcursora) oder [**LoadIcon-Funktion**](/windows/win32/api/winuser/nf-winuser-loadicona) aufrufen, um einen Cursor oder ein Symbol aus den Ressourcen in der ausführbaren Datei (.exe) zu laden und dieses Handle abzurufen.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert in eine **BOOL-Datei** konvertieren und den Wert direkt zurückgeben. Der von der [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) festgelegte **\_ DWL-MSGRESULT-Wert** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
