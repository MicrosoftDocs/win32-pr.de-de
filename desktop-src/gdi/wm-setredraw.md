---
description: Sie senden die **WM_SETREDRAW** an ein Fenster, damit Änderungen in diesem Fenster neu gezeichnet werden können, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593456"
---
# <a name="wm_setredraw-message"></a>WM_SETREDRAW

Sie senden die **WM \_ SETREDRAW-Nachricht** an ein Fenster, um zu ermöglichen, dass Änderungen in diesem Fenster neu gezeichnet werden, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.

Um diese Nachricht zu senden, rufen Sie die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) mit den folgenden Parametern auf.

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a>Parameter

`wParam`

Der neu gezeichnete Zustand. Wenn dieser Parameter **TRUE ist,** kann der Inhalt nach einer Änderung neu gezeichnet werden. Wenn dieser Parameter **FALSE ist,** kann der Inhalt nach einer Änderung nicht neu gezeichnet werden.

`lParam`

Dieser Parameter wird nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Ihre Anwendung sollte 0 zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung kann nützlich sein, wenn Ihre Anwendung einem Listenfeld mehrere Elemente hinzufügen muss. Ihre Anwendung kann diese Nachricht aufrufen, bei der *wParam* auf **FALSE** festgelegt ist, die Elemente hinzufügen und die Nachricht dann erneut aufrufen, während *wParam* auf **TRUE festgelegt ist.** Schließlich kann Ihre Anwendung [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW \_ ERASE \| RDW FRAME \_ \| RDW \_ INVALIDATE \| RDW ALLCHILDREN) \_ aufrufen, damit das Listenfeld neu gezeichnet wird.

> [!NOTE] 
> Sie sollten [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) mit den angegebenen Flags anstelle von [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect)verwenden, da ersteres für einige Steuerelemente erforderlich ist, die einen eigenen Nichtclientbereich haben, oder über Fensterstile verfügen, die dazu führen, dass ihnen ein Nichtclientbereich (z. B. **WS_THICKFRAME,** **WS_BORDER oder** **WS_EX_CLIENTEDGE) erteilt wird.** Wenn das Steuerelement nicht über einen Nichtclientbereich verfügt, führt **RedrawWindow** mit diesen Flags nur so viel Ungültigkeit wie **InvalidateRect** durch.

Durch übergeben **WM_SETREDRAW** meldung an die **DefWindowProc-Funktion** wird der WS_VISIBLE aus dem Fenster entfernt, wenn *wParam* auf **FALSE festgelegt ist.**  Obwohl der Fensterinhalt auf dem Bildschirm sichtbar bleibt, gibt die [**IsWindowVisible-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) **FALSE** zurück, wenn sie in einem Fenster in diesem Zustand aufgerufen wird. 

Durch übergeben **WM_SETREDRAW** meldung an die **DefWindowProc-Funktion** wird dem Fenster der WS_VISIBLE-Stil hinzufügt, sofern nicht festgelegt, wenn *wParam* auf **TRUE festgelegt ist.**  Wenn Ihre Anwendung  die WM_SETREDRAW-Nachricht sendet, bei der *wParam* auf **TRUE** festgelegt ist, wird das Fenster sichtbar. 

**Windows 10 und höher; Windows Server 2016 und höher.** Das System legt eine Eigenschaft namens *SysSetRedraw*  für ein Fenster fest, dessen Fensterprozedur WM_SETREDRAW an **DefWindowProc übergibt.** Sie können die [**GetProp-Funktion**](/windows/win32/api/Winuser/nf-winuser-getpropa) verwenden, um den Eigenschaftswert zu erhalten, wenn er verfügbar ist. **GetProp gibt** einen Wert zurück, der nicht 0 (null) ist, wenn das Neuzeichneten deaktiviert ist. **GetProp** gibt 0 (null) zurück, wenn das neu gezeichnete Fenster aktiviert ist oder die Fenstereigenschaft nicht vorhanden ist. 

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 2000 Professional \[nur Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 2000 Server \[nur Desktop-Apps\] |
| Header | <dl><dt>Winuser.h (include Windows.h)</dt></dl> |

## <a name="see-also"></a>Weitere Informationen

* [Übersicht über Das Zeichnen und Zeichnen](painting-and-drawing.md)
* [Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
* [RedrawWindow](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
