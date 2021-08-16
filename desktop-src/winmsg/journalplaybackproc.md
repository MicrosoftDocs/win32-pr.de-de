---
UID: ''
title: Rückruffunktion JournalPlaybackProc
description: Gibt eine Reihe von Maus- und Tastaturmeldungen wieder, die zuvor aufgezeichnet wurden.
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
ms.openlocfilehash: bee538bf2c20cc3cadb6f0bdf6f5dd6a2ae12dfe8a21baeb56b8ad62cb23ff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437127"
---
# <a name="journalplaybackproc-function"></a>JournalPlaybackProc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) verwendet wird.
In der Regel verwendet eine Anwendung diese Funktion, um eine Reihe von Maus- und Tastaturmeldungen wiederzugeben, die zuvor von der **JournalRecordProc-Hookprozedur** aufgezeichnet wurden.
Solange eine **JournalPlaybackProc-Hookprozedur** installiert ist, sind reguläre Maus- und Tastatureingaben deaktiviert.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**JournalPlaybackProc** ist ein Platzhalter für den anwendungs- oder bibliotheksdefinierte Funktionsnamen.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
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
| **HC_GETNEXT** 1 | Die Hookprozedur muss die aktuelle Maus- oder Tastaturmeldung in die [EVENTMSG-Struktur](/windows/desktop/api/winuser/ns-winuser-eventmsg) kopieren, auf die der *lParam-Parameter* zeigt. |
| **HC_NOREMOVE** 3 | Eine Anwendung hat die [PeekMessage-Funktion](/windows/desktop/api/winuser/nf-winuser-peekmessagew) aufgerufen, wobei wRemoveMsg auf **PM_NOREMOVE** festgelegt ist. Dies bedeutet, dass die Nachricht nach der **PeekMessage-Verarbeitung** nicht aus der Nachrichtenwarteschlange entfernt wird. |
| **HC_NOREMOVE** 2 | Die Hookprozedur muss vorbereiten, um die nächste Maus- oder Tastaturnachricht in die **EVENTMSG-Struktur** zu kopieren, auf die *lParam* zeigt. Nach dem Empfang des **HC_GETNEXT** Codes muss die Hookprozedur die Nachricht in die Struktur kopieren. |
| **HC_SYSMODALOFF** 5 | Ein system modales Dialogfeld wurde zerstört. Die Hookprozedur muss die Wiedergabe der Nachrichten fortsetzen. |
| **HC_SYSMODALON** 4 | Ein system modales Dialogfeld wird angezeigt. Bis das Dialogfeld zerstört wird, muss die Hookprozedur die Wiedergabe von Nachrichten beenden. |

### <a name="wparam"></a>wParam

Typ: **WPARAM**

Dieser Parameter wird nicht verwendet.

### <a name="lparam"></a>lParam

Typ: **LPARAM**

Ein Zeiger auf eine **EVENTMSG-Struktur,** die eine Nachricht darstellt, die von der Hookprozedur verarbeitet wird.
Dieser Parameter ist nur gültig, wenn der *Codeparameter* **HC_GETNEXT** ist.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Damit das System vor der Verarbeitung der Nachricht wartet, muss der Rückgabewert die Zeitspanne in Takten sein, die das System warten soll.

(Dieser Wert kann berechnet werden, indem die Differenz zwischen den Zeitmembern in den aktuellen und vorherigen Eingabenachrichten berechnet wird.)

Um die Nachricht sofort zu verarbeiten, sollte der Rückgabewert 0 (null) sein. Der Rückgabewert wird nur verwendet, wenn der Hookcode **HC_GETNEXT** ist. andernfalls wird sie ignoriert.

## <a name="remarks"></a>Hinweise

Eine **JournalPlaybackProc-Hookprozedur** sollte eine Eingabenachricht in den *Parameter lParam* kopieren.
Die Nachricht muss zuvor mithilfe einer **JournalRecordProc-Hookprozedur** aufgezeichnet worden sein, die die Nachricht nicht ändern sollte.

Um die gleiche Nachricht immer wieder abzurufen, kann die Hookprozedur mehrmals aufgerufen werden, wobei der *Codeparameter* auf **HC_GETNEXT** festgelegt ist, ohne dass ein dazwischen liegender Aufruf mit *Code* auf **HC_SKIP** festgelegt ist.

Wenn *der Code* **HC_GETNEXT** und der Rückgabewert größer als 0 (null) ist, wird das System für die vom Rückgabewert angegebene Anzahl von Millisekunden in den Standbymodus versetzt. Wenn das System fortgesetzt wird, wird die Hookprozedur erneut aufgerufen, wobei *der Code* auf **HC_GETNEXT** festgelegt ist, um dieselbe Nachricht abzurufen.
Der Rückgabewert dieses neuen Aufrufs von **JournalPlaybackProc** sollte 0 (null) sein. Andernfalls wird das System für die durch den Rückgabewert angegebene Anzahl von Millisekunden wieder in den Standbymodus versetzt, **JournalPlaybackProc** erneut aufrufen usw.
Das System reagiert anscheinend nicht.

Im Gegensatz zu den meisten anderen globalen Hookprozidents werden die Hookprozes **JournalRecordProc** und **JournalPlaybackProc** immer im Kontext des Threads aufgerufen, der den Hook festgelegt hat.

Nachdem die Hookprozedur die Steuerung an das System zurückgegeben hat, wird die Nachricht weiterhin verarbeitet. Wenn *Code* **HC_SKIP** ist, muss die Hookprozedur vorbereiten, um die nächste aufgezeichnete Ereignisnachricht beim nächsten Aufruf zurückzugeben.

Installieren Sie die **JournalPlaybackProc-Hookprozedur,** indem Sie den [WH_JOURNALPLAYBACK](about-hooks.md) Typ und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angeben.

Wenn der Benutzer während der Journalwiedergabe STRG+ESC ODER STRG+ALT+ENTF drückt, beendet das System die Wiedergabe, enthookt die Journalwiedergabeprozedur und sendet eine [WM_CANCELJOURNAL](wm-canceljournal.md) Meldung an die Journalanwendung.

Wenn die Hookprozedur eine Nachricht im **Bereich** WM_KEYFIRST **WM_KEYLAST** zurückgibt, gelten die folgenden Bedingungen:

* Der **paramL-Member** der **EVENTMSG-Struktur** gibt den virtuellen Schlüsselcode der gedrückten Taste an.
* Der **paramH-Member** der **EVENTMSG-Struktur** gibt den Scancode an.
* Es gibt keine Möglichkeit, eine Wiederholungsanzahl anzugeben.
Das -Ereignis wird immer zur Darstellung eines Schlüsselereignisses übernommen.

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hooks](hooks.md)
