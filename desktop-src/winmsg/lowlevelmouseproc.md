---
UID: ''
title: Lowlevelmousproc-Rückruffunktion
description: Das System ruft diese Funktion jedes Mal auf, wenn ein neues Mauseingabe Ereignis in einer Thread Eingabe Warteschlange gepostet wird.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2020
ms.locfileid: "104039793"
---
# <a name="lowlevelmouseproc-function"></a>Lowlevelmousproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Das System ruft diese Funktion jedes Mal auf, wenn ein neues Mauseingabe Ereignis in einer Thread Eingabe Warteschlange gepostet wird.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Lowlevelmouseproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

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

Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Maus Meldung. |

### <a name="wparam-in"></a>wParam [in]

Typ: **wParam**

Der Bezeichner der Maus Nachricht.
Dieser Parameter kann eine der folgenden Meldungen sein: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) oder [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [msllhuokstruct](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) -Struktur.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *nCode* größer als oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_MOUSE_LL](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.
Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hook-Kette oder der Zielfenster Prozedur übergibt.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_MOUSE_LL** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.

Dieser Hook wird im Kontext des Threads aufgerufen, der ihn installiert hat.
Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.
Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.

Die Mauseingabe kann aus dem lokalen Mauszeiger oder aus Aufrufen der [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) -Funktion stammen.
Wenn die Eingabe aus einem **mouse_event** aufgerufen wird, wurde die Eingabe "eingefügt".
Allerdings wird der **WH_MOUSE_LL** Hook nicht in einen anderen Prozess eingefügt.
Stattdessen schaltet der Kontext zum Prozess zurück, der den Hook installiert hat, und wird im ursprünglichen Kontext aufgerufen.
Anschließend wechselt der Kontext zurück zu der Anwendung, die das Ereignis generiert hat.

Die Hook-Prozedur sollte eine Nachricht in kürzerer Zeit **als der im** folgenden Registrierungsschlüssel angegebene Dateneintrag verarbeiten: **HKEY_CURRENT_USER\Control Panel\Desktop**.

Der Wert ist in Millisekunden angegeben.
Wenn für die Hook-Prozedur ein Timeout eintritt, übergibt das System die Nachricht an den nächsten Hook.
Allerdings wird der Hook unter Windows 7 und höher automatisch entfernt, ohne aufgerufen zu werden.
Es gibt keine Möglichkeit, dass die Anwendung weiß, ob der Hook entfernt wurde.

**Hinweis:**  Debughooks können diesen Typ von Maus Hooks mit niedriger Ebene nicht verfolgen.
Wenn die Anwendung Low-Level-Hooks verwenden muss, sollte Sie die Hooks in einem dedizierten Thread ausführen, der die Arbeit an einen Arbeits Thread übergibt und dann sofort zurückgibt.
In den meisten Fällen, in denen die Anwendung Low-Level-Hooks verwenden muss, sollte Sie stattdessen unformatierte Eingaben überwachen.
Dies liegt daran, dass die Eingabe von Rohdaten die Maus-und Tastatur Meldungen, die auf andere Threads abzielen, effektiver als auf Low-Level-Hooks abzielen können.
Weitere Informationen zur [roheingabe finden](/windows/desktop/inputdev/raw-input)Sie unter unformatierte Eingaben.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[Kbdlltuokstruct](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[Msllhuokstruct](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Hooks](hooks.md)

[Informationen zu Hooks](about-hooks.md)
