---
description: Wird an ein Fenster gesendet, wenn die Größe oder Position des Fensters geändert wird. Eine Anwendung kann diese Nachricht verwenden, um die standardmäßige maximierte Größe und Position des Fensters zu überschreiben, bzw. die standardmäßige oder maximale nach Verfolgungs Größe.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: WM_GETMINMAXINFO Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866759"
---
# <a name="wm_getminmaxinfo-message"></a>WM \_ getminmaxinfo-Meldung

Wird an ein Fenster gesendet, wenn die Größe oder Position des Fensters geändert wird. Eine Anwendung kann diese Nachricht verwenden, um die standardmäßige maximierte Größe und Position des Fensters zu überschreiben, bzw. die standardmäßige oder maximale nach Verfolgungs Größe.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**minmaxinfo**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) -Struktur, die die standardmäßige maximierte Position und die Standardabmessungen sowie die Standard-und maximale nach Verfolgungs Größe enthält. Eine Anwendung kann die Standardwerte überschreiben, indem die Elemente dieser Struktur festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die maximale nach Verfolgungs Größe ist die größte Fenstergröße, die erstellt werden kann, indem die Rahmen verwendet werden, um das Fenster zu verkleinern. Die Mindestgröße für die Nachverfolgung ist die kleinste Fenstergröße, die mithilfe der Rahmengröße des Fensters erstellt werden kann.

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

[**Fenster**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
