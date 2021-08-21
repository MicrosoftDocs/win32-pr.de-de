---
UID: ''
title: KeyboardProc-Rückruffunktion
description: Das System ruft diese Funktion auf und ruft eine Meldungsfunktion ab, und es muss eine Tastaturnachricht verarbeitet werden.
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
ms.openlocfilehash: ed2f3943667d09f42a7bc843adac69eaa4043454d93b409b193513b8ab43fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437155"
---
# <a name="keyboardproc-function"></a>KeyboardProc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) verwendet wird.
Das System ruft diese Funktion immer dann auf, wenn eine Anwendung die [GetMessage-](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [PeekMessage-Funktion](/windows/desktop/api/winuser/nf-winuser-peekmessagew) aufruft und eine Tastaturnachricht ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) oder [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) verarbeitet werden soll.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**KeyboardProc** ist ein Platzhalter für den anwendungs- oder bibliotheksdefinierte Funktionsnamen.

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

Ein Code, der von der Hookprozedur verwendet wird, um zu bestimmen, wie die Nachricht verarbeitet wird.
Wenn *der Code* kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und sollte den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Die *Parameter wParam* und *lParam* enthalten Informationen zu einer Tastatureingabenachricht. |
| **HC_NOREMOVE** 3 | Die *Parameter wParam* und *lParam* enthalten Informationen zu einer Tastatureingabenachricht, und die Tastatureingabenachricht wurde nicht aus der Nachrichtenwarteschlange entfernt. (Eine Anwendung namens **PeekMessage-Funktion,** die das **flag PM_NOREMOVE** angibt.) |

### <a name="wparam-in"></a>wParam [in]

Typ: **WPARAM**

Der [Virtuelle Schlüsselcode](/windows/desktop/inputdev/virtual-key-codes) des Schlüssels, der die Tastatureingabenachricht generiert hat.

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Wiederholungsanzahl, Scancode, Flag für erweiterte Schlüssel, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag.
Weitere Informationen zum *lParam-Parameter* finden Sie unter [Tastatureingabe-Meldungsflags.](/windows/desktop/inputdev/about-keyboard-input)
In der folgenden Tabelle werden die Bits dieses Werts beschrieben.

| Bits | BESCHREIBUNG |
|-------|---------|
| 0-15 | Die Wiederholungsanzahl. Der Wert gibt an, wie oft die Tastatureingabe wiederholt wird, wenn der Benutzer den Schlüssel gedrückt hält. |
| 16-23 | Der Scancode. Der Wert hängt vom OEM ab. |
| 24 | Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. B. ein Funktionsschlüssel oder ein Schlüssel auf der numerischen Tastatur. Der Wert ist 1, wenn der Schlüssel ein erweiterter Schlüssel ist. Andernfalls ist es 0. |
| 25-28 | Reserviert. |
| 29 | Der Kontextcode. Der Wert ist 1, wenn die ALT-Taste nicht aktiviert ist. Andernfalls ist es 0. |
| 30 | Der vorherige Schlüsselzustand. Der Wert ist 1, wenn der Schlüssel ausgeschaltet ist, bevor die Nachricht gesendet wird. ist 0, wenn der Schlüssel hoch ist. |
| 31 | Der Übergangszustand. Der Wert ist 0, wenn die Taste gedrückt wird, und 1, wenn sie losgelassen wird. |

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *der Code* kleiner als 0 (null) ist, muss die Hookprozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *der Code* größer oder gleich 0 (null) ist und die Hookprozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_KEYBOARD](about-hooks.md) Hooks installiert haben, keine Hookbenachrichtigungen und verhalten sich daher möglicherweise falsch.
Wenn die Hookprozedur die Nachricht verarbeitet hat, wird möglicherweise ein Wert ungleich 0 zurückgegeben, um zu verhindern, dass das System die Nachricht an den Rest der Hookkette oder die Zielfensterprozedur übergibt.

## <a name="remarks"></a>Hinweise

Eine Anwendung installiert die Hookprozedur, indem sie den **WH_KEYBOARD** Hooktyp und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angibt.

Dieser Hook kann im Kontext des Threads aufgerufen werden, der ihn installiert hat.
Der Aufruf erfolgt durch Senden einer Nachricht an den Thread, der den Hook installiert hat.
Daher muss der Thread, der den Hook installiert hat, über eine Meldungsschleife verfügen.

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[Wm_keydown](/windows/desktop/inputdev/wm-keydown)

[Hooks](hooks.md)
