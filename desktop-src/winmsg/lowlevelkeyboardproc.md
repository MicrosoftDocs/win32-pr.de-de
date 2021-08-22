---
UID: ''
title: LowLevelKeyboardProc-Rückruffunktion
description: Das System ruft diese Funktion jedes Mal auf, wenn ein neues Tastatureingabeereignis in eine Threadeingabewarteschlange gesendet wird.
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
ms.openlocfilehash: 5a9a2a0cb5ccf60fe5cfc9f495b621669ba1d85ca04eeb7ecd345cdc60d48bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548570"
---
# <a name="lowlevelkeyboardproc-function"></a>LowLevelKeyboardProc-Funktion

## <a name="description"></a>Beschreibung

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion verwendet](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) wird.
Das System ruft diese Funktion jedes Mal auf, wenn ein neues Tastatureingabeereignis in eine Threadeingabewarteschlange gesendet wird.

**Hinweis:**  Wenn diese Rückruffunktion als Reaktion auf eine Änderung des Zustands eines Schlüssels aufgerufen wird, wird die Rückruffunktion aufgerufen, bevor der asynchrone Zustand des Schlüssels aktualisiert wird.
Folglich kann der asynchrone Zustand des Schlüssels nicht durch Aufrufen von [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) innerhalb der Rückruffunktion bestimmt werden.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**LowLevelKeyboardProc** ist ein Platzhalter für den anwendungs- oder bibliotheksdefinierten Funktionsnamen.

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="code-in"></a>Code [in]

Typ: **int**

Ein Code, mit dem die Hookprozedur bestimmt, wie die Nachricht zu verarbeiten ist.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Die *Parameter wParam* *und lParam* enthalten Informationen zu einer Tastaturmeldung. |

### <a name="wparam-in"></a>wParam [in]

Typ: **WPARAM**

Der Bezeichner der Tastaturmeldung.
Dieser Parameter kann eine der folgenden Meldungen sein: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)oder [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [KBDLLHOOKSTRUCT-Struktur.](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *nCode kleiner* als 0 (null) ist, muss die Hookprozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *nCode* größer oder gleich 0 (null) ist und die Hookprozedur die Nachricht nicht verarbeiten konnte, wird dringend empfohlen, **CallNextHookEx** aufrufen und den zurückgegebenen Wert zurückgibt. Andernfalls erhalten andere [](about-hooks.md) Anwendungen, die WH_KEYBOARD_LL Hooks installiert haben, keine Hookbenachrichtigungen und verhalten sich möglicherweise falsch.
Wenn die Hookprozedur die Nachricht verarbeitet hat, wird möglicherweise ein Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hookkette oder die Zielfensterprozedur übergehen kann.

## <a name="remarks"></a>Hinweise

Eine Anwendung installiert die Hookprozedur, indem WH_KEYBOARD_LL Hooktyp und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angeben. 

Dieser Hook wird im Kontext des Threads aufgerufen, der ihn installiert hat.
Der Aufruf erfolgt durch Senden einer Nachricht an den Thread, der den Hook installiert hat.
Daher muss der Thread, der den Hook installiert hat, über eine Meldungsschleife verfügen.

Die Tastatureingabe kann vom lokalen Tastaturtreiber oder von Aufrufen der keybd_event [werden.](/windows/desktop/api/winuser/nf-winuser-keybd_event)
Wenn die Eingabe aus einem Aufruf von keybd_event **stammt,** wurde die Eingabe "eingefügt".
Der WH_KEYBOARD_LL hook wird jedoch nicht in einen anderen Prozess eingefügt.
Stattdessen wechselt der Kontext zurück zum Prozess, der den Hook installiert hat, und wird im ursprünglichen Kontext aufgerufen.
Anschließend wechselt der Kontext zurück zu der Anwendung, die das Ereignis generiert hat.

Die Hookprozedur sollte eine Nachricht in weniger Zeit verarbeiten als der Im **LowLevelHooksTimeout-Wert** im folgenden Registrierungsschlüssel **angegebene Dateneintrag:HKEY_CURRENT_USER\Control Panel\Desktop.**

Der Wert ist in Millisekunden angegeben.
Wenn für die Hookprozedur ein Zeitablauf besteht, übergibt das System die Nachricht an den nächsten Hook.
Allerdings wird Windows 7 und höher automatisch entfernt, ohne aufgerufen zu werden.
Die Anwendung kann nicht wissen, ob der Hook entfernt wird.

Hinweis: Debughooks können diese Art von Tastaturhooks auf niedriger Ebene nicht nachverfolgen.
Wenn die Anwendung Hooks auf niedriger Ebene verwenden muss, sollte sie die Hooks in einem dedizierten Thread ausführen, der die Arbeit an einen Arbeitsthread übergibt und dann sofort zurückgibt.
In den meisten Fällen, in denen die Anwendung Hooks auf niedriger Ebene verwenden muss, sollte sie stattdessen rohe Eingaben überwachen.
Dies liegt daran, dass Unformatierungseingaben Maus- und Tastaturmeldungen asynchron überwachen können, die für andere Threads effektiver als Hooks auf niedriger Ebene ausgerichtet sind.
Weitere Informationen zu rohen Eingaben finden Sie unter [Rohdateneingabe.](/windows/desktop/inputdev/raw-input)

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Wm_keydown](/windows/desktop/inputdev/wm-keydown)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)

[WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup)

[Hooks](hooks.md)

[Informationen zu Hooks](about-hooks.md)
