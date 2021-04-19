---
UID: ''
title: Keyboardproc-Rückruffunktion
description: Das System ruft diese Funktion auf und ruft eine Message-Funktion ab, und es gibt eine zu verarbeitende Tastatur Meldung.
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
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106342122"
---
# <a name="keyboardproc-function"></a>Keyboardproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Das System ruft diese Funktion immer dann auf, wenn eine Anwendung die [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) -oder die [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) -Funktion aufruft und eine Tastatur Meldung ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) oder [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) zur Verarbeitung vorhanden ist.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Keyboardproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="code-in"></a>Code [in]

Typ: **int**

Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.
Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Tastatureingabe-Nachricht. |
| **HC_NOREMOVE** 3 | Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Tastatureingabe-Nachricht, und die Tastatureingabe-Nachricht wurde nicht aus der Nachrichten Warteschlange entfernt. (Eine Anwendung, die die Funktion " **Peer Message** " genannt wird und das **PM_NOREMOVE** Flag angibt.) |

### <a name="wparam-in"></a>wParam [in]

Typ: **wParam**

Der [Code](/windows/desktop/inputdev/virtual-key-codes) für den virtuellen Schlüssel des Schlüssels, der die Tastatureingabe-Nachricht generiert hat.

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das transitionstate-Flag.
Weitere Informationen zum *LPARAM* -Parameter finden Sie unter [KeyStroke-Nachrichtenflags](/windows/desktop/inputdev/about-keyboard-input).
In der folgenden Tabelle werden die Bits dieses Werts beschrieben.

| Bits | BESCHREIBUNG |
|-------|---------|
| 0-15 | Die Wiederholungs Anzahl. Der Wert gibt an, wie oft der Tastatur Schlag wiederholt wird, wenn der Benutzer die Taste gedrückt hält. |
| 16-23 | Der Überprüfungs Code. Der Wert hängt vom OEM ab. |
| 24 | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. ein Funktionsschlüssel oder ein Schlüssel auf der numerischen Keypad. Der Wert ist 1, wenn der Schlüssel ein erweiterter Schlüssel ist. Andernfalls ist der Wert 0. |
| 25-28 | Reserviert. |
| 29 | Der Kontext Code. Der Wert ist 1, wenn die Alt-Taste gedrückt ist. Andernfalls ist der Wert 0. |
| 30 | Der vorherige Schlüssel Zustand. Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird. der Wert ist 0 (null), wenn der Schlüssel aktuell ist. |
| 31 | Der Übergangszustand. Der Wert ist 0 (null), wenn der Schlüssel gedrückt wird, und 1, wenn er freigegeben wird. |

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *Code* größer oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_KEYBOARD](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.
Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hook-Kette oder der Zielfenster Prozedur übergibt.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_KEYBOARD** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.

Dieser Hook kann im Kontext des Threads aufgerufen werden, der ihn installiert hat.
Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.
Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[Hooks](hooks.md)
