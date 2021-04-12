---
description: Wird an ein minimiertes (legendäres) Fenster gesendet.
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: WM_QUERYDRAGICON Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345579"
---
# <a name="wm_querydragicon-message"></a>WM \_ querydragicon-Meldung

Wird an ein minimiertes (legendäres) Fenster gesendet. Das Fenster wird vom Benutzer gezogen, aber es ist kein Symbol für seine Klasse definiert. Eine Anwendung kann ein Handle für ein Symbol oder einen Cursor zurückgeben. Das System zeigt diesen Cursor oder dieses Symbol an, während der Benutzer das Symbol zieht.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Eine Anwendung sollte ein Handle für einen Cursor oder ein Symbol zurückgeben, den das System anzeigen soll, während der Benutzer das Symbol zieht. Der Cursor oder das Symbol muss mit der Auflösung des Anzeige Treibers kompatibel sein. Wenn die Anwendung **null** zurückgibt, zeigt das System den Standard Cursor an.

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer das Symbol eines Fensters ohne ein Klassen Symbol zieht, ersetzt das System das Symbol durch einen Standard Cursor. Wenn die Anwendung erfordert, dass während des Zieh Punkts ein anderer Cursor angezeigt wird, muss ein Handle für den Cursor oder das Symbol zurückgegeben werden, das mit der Auflösung des Anzeige Treibers kompatibel ist. Wenn eine Anwendung ein Handle für einen Farb Cursor oder ein Symbol zurückgibt, konvertiert das System den Cursor oder das Symbol in schwarz und weiß. Die Anwendung kann die [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) -oder [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) -Funktion aufrufen, um einen Cursor oder ein Symbol aus den Ressourcen in der ausführbaren Datei (. exe) zu laden und dieses Handle abzurufen.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben. Der von der [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
