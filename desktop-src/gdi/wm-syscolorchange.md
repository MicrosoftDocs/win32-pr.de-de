---
description: Die WM SYSCOLORCHANGE-Meldung wird an alle Fenster der obersten Ebene gesendet, wenn eine Änderung an einer \_ Systemfarbeinstellung vorgenommen wird.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: WM_SYSCOLORCHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e39ff8b5189da1a4cf48b7f6923c1cf12e8f30aa20fb26457d54a3f01d1b5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118483099"
---
# <a name="wm_syscolorchange-message"></a>WM \_ SYSCOLORCHANGE-Meldung

Die **WM \_ SYSCOLORCHANGE-Meldung** wird an alle Fenster der obersten Ebene gesendet, wenn eine Änderung an einer Systemfarbeinstellung vorgenommen wird.

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

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das System sendet eine [**WM \_ PAINT-Nachricht**](wm-paint.md) an jedes Fenster, das von einer Änderung der Systemfarbe betroffen ist.

Anwendungen mit Pinseln, die die vorhandenen Systemfarben verwenden, sollten diese Pinsel löschen und mit den neuen Systemfarben neu erstellen.

Fenster auf oberster Ebene, die allgemeine Steuerelemente verwenden, müssen die **WM \_ SYSCOLORCHANGE-Meldung** an die Steuerelemente weitersennen. Andernfalls werden die Steuerelemente nicht über die Farbänderung benachrichtigt. Dadurch wird sichergestellt, dass die von Ihren allgemeinen Steuerelementen verwendeten Farben mit denen anderer Benutzeroberflächenobjekte konsistent sind. Beispielsweise verwendet ein Symbolleisten-Steuerelement die Farbe "3D-Objekte", um seine Schaltflächen zu zeichnen. Wenn der Benutzer die Farbe der 3D-Objekte ändert, die **WM \_ SYSCOLORCHANGE-Meldung** jedoch nicht an die Symbolleiste weitergeleitet wird, verbleiben die Symbolleistenschaltflächen in ihrer ursprünglichen Farbe, während sich die Farbe anderer Schaltflächen im System ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farbmeldungen](color-messages.md)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> </dl>

 

 
