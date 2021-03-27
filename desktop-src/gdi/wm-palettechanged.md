---
description: Die "WM \_ palettechanged"-Meldung wird an alle Fenster der obersten Ebene und überlappende Fenster gesendet, nachdem das Fenster mit dem Tastaturfokus seine logische Palette erreicht hat und dadurch die Systempalette geändert wurde.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: WM_PALETTECHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755824"
---
# <a name="wm_palettechanged-message"></a>WM \_ palettechanged-Meldung

Die " **WM \_ palettechanged** "-Meldung wird an alle Fenster der obersten Ebene und überlappende Fenster gesendet, nachdem das Fenster mit dem Tastaturfokus seine logische Palette erreicht hat und dadurch die Systempalette geändert wurde. Diese Meldung ermöglicht ein Fenster, das eine Farbpalette verwendet, aber nicht den Tastaturfokus hat, um seine logische Palette zu erkennen und den Client Bereich zu aktualisieren.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Ein Handle für das Fenster, das bewirkt hat, dass die Systempalette geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Nachricht muss an alle Fenster der obersten Ebene und überlappende Fenster gesendet werden, einschließlich derjenigen, die die Systempalette geändert hat. Wenn ein untergeordnetes Fenster eine Farbpalette verwendet, muss diese Meldung ebenfalls an Sie weitergegeben werden.

Um das Erstellen einer Endlosschleife zu vermeiden, darf ein Fenster, das diese Nachricht empfängt, seine Palette nicht erkennen, es sei denn, es wird festgelegt, dass *wParam* kein eigenes Fenster Handle enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farb Meldungen](color-messages.md)
</dt> <dt>

[**WM- \_ paletteischanging**](wm-paletteischanging.md)
</dt> <dt>

[**WM \_ querynewpalette**](wm-querynewpalette.md)
</dt> </dl>

 

 
