---
description: Die WM PALETTECHANGED-Nachricht wird an alle Fenster der obersten Ebene gesendet und überlappen, nachdem das Fenster mit dem Tastaturfokus seine logische Palette erkannt und dadurch die \_ Systempalette geändert hat.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: WM_PALETTECHANGED (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb706452e357f2e322b1f4e2618f0fd59c5c4d9a6606c07d18fae7c3b346323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977920"
---
# <a name="wm_palettechanged-message"></a>WM \_ PALETTECHANGED-Nachricht

Die **WM \_ PALETTECHANGED-Nachricht** wird an alle Fenster der obersten Ebene gesendet und überlappen, nachdem das Fenster mit dem Tastaturfokus seine logische Palette erkannt und dadurch die Systempalette geändert hat. Diese Meldung ermöglicht einem Fenster, das eine Farbpalette verwendet, aber nicht über den Tastaturfokus verfügt, um seine logische Palette zu realisieren und seinen Clientbereich zu aktualisieren.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, durch das sich die Systempalette geändert hat.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Meldung muss an alle Fenster der obersten Ebene und überlappende Fenster gesendet werden, einschließlich des Fensters, das die Systempalette geändert hat. Wenn untergeordnete Fenster eine Farbpalette verwenden, muss diese Meldung auch an sie übergeben werden.

Um zu vermeiden, dass eine Endlosschleife erstellt wird, darf ein Fenster, das diese Nachricht empfängt, seine Palette nicht erkennen, es sei denn, es bestimmt, dass *wParam* kein eigenes Fensterhandli enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farbmeldungen](color-messages.md)
</dt> <dt>

[**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
