---
description: Die WM- \_ syscolorchange-Meldung wird an alle Fenster der obersten Ebene gesendet, wenn eine Änderung an einer System Farbeinstellung vorgenommen wird.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: WM_SYSCOLORCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980792"
---
# <a name="wm_syscolorchange-message"></a>WM- \_ syscolorchange-Meldung

Die **WM- \_ syscolorchange** -Meldung wird an alle Fenster der obersten Ebene gesendet, wenn eine Änderung an einer System Farbeinstellung vorgenommen wird.

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

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das System sendet eine [**WM \_**](wm-paint.md) -Zeichnungs Meldung an jedes Fenster, das von einer System Farbänderung betroffen ist.

Anwendungen mit Pinseln, die die vorhandenen Systemfarben verwenden, sollten diese Pinsel löschen und mithilfe der neuen Systemfarben neu erstellen.

Fenster der obersten Ebene, die allgemeine Steuerelemente verwenden, müssen die **WM- \_ syscolorchange** -Meldung an die Steuerelemente weiterleiten. andernfalls werden die Steuerelemente nicht über die Farbänderung benachrichtigt. Dadurch wird sichergestellt, dass die von den allgemeinen Steuerelementen verwendeten Farben mit den Farben übereinstimmen, die von anderen Benutzeroberflächen Objekten verwendet werden. Beispielsweise verwendet ein ToolBar-Steuerelement die Farbe "3D-Objekte", um seine Schaltflächen zu zeichnen. Wenn der Benutzer die 3D-Objekt Farbe ändert, aber die **WM- \_ syscolorchange** -Meldung nicht an die Symbolleiste weitergeleitet wird, bleiben die Schaltflächen der Symbolleiste in der ursprünglichen Farbe, während sich die Farbe anderer Schaltflächen im System ändert.

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

[**WM- \_ Paint**](wm-paint.md)
</dt> </dl>

 

 
