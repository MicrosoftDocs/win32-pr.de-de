---
UID: ''
title: LowLevelMouseProc-Rückruffunktion
description: Das System ruft diese Funktion jedes Mal auf, wenn ein neues Mauseingabeereignis in eine Threadeingabewarteschlange gesendet wird.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 53f75d14395388ce22ce86ef73f8819892c3fe7285909b1f38c801af476636a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705786"
---
# <a name="lowlevelmouseproc-function"></a>LowLevelMouseProc-Funktion

## <a name="description"></a>Beschreibung

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion verwendet](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) wird.
Das System ruft diese Funktion jedes Mal auf, wenn ein neues Mauseingabeereignis in eine Threadeingabewarteschlange gesendet wird.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**LowLevelMouseProc** ist ein Platzhalter für den anwendungs- oder bibliotheksdefinierten Funktionsnamen.

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="ncode-in"></a>nCode [in]

Typ: **int**

Ein Code, mit dem die Hookprozedur bestimmt, wie die Nachricht zu verarbeiten ist.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Die *Parameter wParam* *und lParam* enthalten Informationen zu einer Mausmeldung. |

### <a name="wparam-in"></a>wParam [in]

Typ: **WPARAM**

Der Bezeichner der Mausmeldung.
Dieser Parameter kann eine der folgenden Meldungen sein: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) [oder WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [MSLLHOOKSTRUCT-Struktur.](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *nCode kleiner* als 0 (null) ist, muss die Hookprozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *nCode* größer oder gleich 0 (null) ist und die Hookprozedur die Nachricht nicht verarbeiten konnte, wird dringend empfohlen, **CallNextHookEx** aufrufen und den zurückgegebenen Wert zurückgibt. Andernfalls erhalten andere [](about-hooks.md) Anwendungen, die WH_MOUSE_LL Hooks installiert haben, keine Hookbenachrichtigungen und verhalten sich möglicherweise falsch.
Wenn die Hookprozedur die Nachricht verarbeitet hat, wird möglicherweise ein Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hookkette oder die Zielfensterprozedur übergehen kann.

## <a name="remarks"></a>Hinweise

Eine Anwendung installiert die Hookprozedur, indem sie WH_MOUSE_LL Hooktyp und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** an. 

Dieser Hook wird im Kontext des Threads aufgerufen, der ihn installiert hat.
Der Aufruf erfolgt durch Senden einer Nachricht an den Thread, der den Hook installiert hat.
Daher muss der Thread, der den Hook installiert hat, über eine Meldungsschleife verfügen.

Die Mauseingabe kann vom lokalen Maustreiber oder von Aufrufen der mouse_event [werden.](/windows/desktop/api/winuser/nf-winuser-mouse_event)
Wenn die Eingabe aus einem Aufruf von mouse_event **stammt,** wurde die Eingabe "eingefügt".
Der **WH_MOUSE_LL** hook wird jedoch nicht in einen anderen Prozess eingefügt.
Stattdessen wechselt der Kontext zurück zum Prozess, der den Hook installiert hat, und wird im ursprünglichen Kontext aufgerufen.
Anschließend wechselt der Kontext zurück zu der Anwendung, die das Ereignis generiert hat.

Die Hookprozedur sollte eine Nachricht in weniger Zeit verarbeiten als der Im **LowLevelHooksTimeout-Wert** im folgenden Registrierungsschlüssel **angegebene Dateneintrag:HKEY_CURRENT_USER\Control Panel\Desktop**.

Der Wert ist in Millisekunden angegeben.
Wenn für die Hookprozedur ein Zeitablauf besteht, übergibt das System die Nachricht an den nächsten Hook.
Allerdings wird Windows 7 und höher automatisch entfernt, ohne aufgerufen zu werden.
Die Anwendung kann nicht wissen, ob der Hook entfernt wird.

**Hinweis:**  Debughooks können diese Art von Maushooks auf niedriger Ebene nicht nachverfolgen.
Wenn die Anwendung Hooks auf niedriger Ebene verwenden muss, sollte sie die Hooks in einem dedizierten Thread ausführen, der die Arbeit an einen Arbeitsthread übergibt und dann sofort zurückgibt.
In den meisten Fällen, in denen die Anwendung Hooks auf niedriger Ebene verwenden muss, sollte sie stattdessen rohe Eingaben überwachen.
Dies liegt daran, dass Unformatierungseingaben Maus- und Tastaturmeldungen asynchron überwachen können, die für andere Threads effektiver als Hooks auf niedriger Ebene ausgerichtet sind.
Weitere Informationen zu rohen Eingaben finden Sie unter [Rohdateneingabe.](/windows/desktop/inputdev/raw-input)

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[Wm_lbuttonup](/windows/desktop/inputdev/wm-lbuttonup)

[Wm_mousemove](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Hooks](hooks.md)

[Informationen zu Hooks](about-hooks.md)
