---
UID: ''
title: MouseProc-Rückruffunktion
description: Das System ruft diese Funktion auf, wenn eine Anwendung eine Nachrichtenfunktion aufruft und eine Mausnachricht verarbeitet werden soll.
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
ms.openlocfilehash: fa1528ce2910e563e3fe930fe19960aa43b437b22c53c03d0febc51b98bcc55b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200691"
---
# <a name="mouseproc-function"></a>MouseProc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion verwendet](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) wird.
Das System ruft diese Funktion auf, wenn eine Anwendung die [GetMessage-](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [PeekMessage-Funktion](/windows/desktop/api/winuser/nf-winuser-peekmessagew) aufruft und eine Mausnachricht verarbeitet werden soll.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**MouseProc ist** ein Platzhalter für den anwendungs- oder bibliotheksdefinierten Funktionsnamen.

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="ncode-in"></a>nCode [in]

Typ: **int**

Ein Code, der von der Hookprozedur verwendet wird, um zu bestimmen, wie die Nachricht zu verarbeiten ist.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Die *Parameter wParam* *und lParam* enthalten Informationen zu einer Mausmeldung. |
| **HC_NOREMOVE** 3 | Die *Parameter wParam* und *lParam* enthalten Informationen zu einer Mausmeldung, und die Mausnachricht wurde nicht aus der Nachrichtenwarteschlange entfernt. (Eine Anwendung namens **PeekMessage-Funktion,** die das **PM_NOREMOVE** an.) |

### <a name="wparam-in"></a>wParam [in]

Typ: **WPARAM**

Der Bezeichner der Mausmeldung.

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [MOUSEHOOKSTRUCT-Struktur.](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *nCode kleiner* als 0 (null) ist, muss die Hookprozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *nCode* größer oder gleich 0 (null) ist und die Hookprozedur die Nachricht nicht verarbeiten konnte, wird dringend empfohlen, **CallNextHookEx** auf aufruft und den zurückgegebenen Wert zurückgibt. Andernfalls erhalten andere [](about-hooks.md) Anwendungen, die WH_MOUSE Hooks installiert haben, keine Hookbenachrichtigungen und verhalten sich möglicherweise falsch.
Wenn die Hookprozedur die Nachricht verarbeitet hat, wird möglicherweise ein Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an die Zielfensterprozedur übergehen kann.

## <a name="remarks"></a>Hinweise

Eine Anwendung installiert die Hookprozedur, indem WH_MOUSE Hooktyp und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angeben.

Die Hookprozedur darf keine [WH_JOURNALPLAYBACK](about-hooks.md) Rückruffunktion installieren.

Dieser Hook kann im Kontext des Threads aufgerufen werden, der ihn installiert hat.
Der Aufruf erfolgt durch Senden einer Nachricht an den Thread, der den Hook installiert hat.
Daher muss der Thread, der den Hook installiert hat, über eine Meldungsschleife verfügen.

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)

[Informationen zu Hooks](about-hooks.md)
