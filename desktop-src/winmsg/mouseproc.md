---
UID: ''
title: Mousproc-Rückruffunktion
description: Das System ruft diese Funktion auf, wenn eine Anwendung eine Nachrichten Funktion aufruft und eine zu verarbeitende Maus Nachricht vorhanden ist.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106338654"
---
# <a name="mouseproc-function"></a>Mousproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Das System ruft diese Funktion immer dann auf, wenn eine Anwendung die [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) -oder die [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) -Funktion aufruft und eine zu verarbeitende Maus Nachricht vorhanden ist.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Mouseproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

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

Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet werden soll.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Maus Meldung. |
| **HC_NOREMOVE** 3 | Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Maus Meldung, und die Maus Nachricht wurde nicht aus der Nachrichten Warteschlange entfernt. (Eine Anwendung, die die Funktion " **Peer Message** " genannt wird und das **PM_NOREMOVE** Flag angibt.) |

### <a name="wparam-in"></a>wParam [in]

Typ: **wParam**

Der Bezeichner der Maus Nachricht.

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [mouethuokstruct](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) -Struktur.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *nCode* größer als oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_MOUSE](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.
Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an die Zielfenster Prozedur übergibt.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung installiert die Hook-Prozedur, indem Sie den WH_MOUSE Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.

Die Hook-Prozedur darf keine [WH_JOURNALPLAYBACK](about-hooks.md) Rückruffunktion installieren.

Dieser Hook kann im Kontext des Threads aufgerufen werden, der ihn installiert hat.
Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.
Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[Mouselhuokstruct](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)

[Informationen zu Hooks](about-hooks.md)
