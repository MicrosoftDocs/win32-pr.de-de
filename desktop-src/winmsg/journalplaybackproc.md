---
UID: ''
title: Journalplaybackproc-Rückruffunktion
description: Gibt eine Reihe von Maus-und Tastatur Meldungen wieder, die zuvor aufgezeichnet wurden.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "104390107"
---
# <a name="journalplaybackproc-function"></a>Journalplaybackproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
In der Regel verwendet eine Anwendung diese Funktion, um eine Reihe von Maus-und Tastatur Meldungen wiederzugeben, die zuvor von der **journalrecordproc** -Hook-Prozedur aufgezeichnet wurden.
Solange eine **journalplaybackproc** -Hook-Prozedur installiert ist, sind normale Maus-und Tastatureingaben deaktiviert.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Journalplaybackproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

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

Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.
Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_GETNEXT** 1 | Die Hook-Prozedur muss die aktuelle Maus-oder Tastatur Nachricht in die [eventmsg](/windows/desktop/api/winuser/ns-winuser-eventmsg) -Struktur kopieren, auf die durch den *LPARAM* -Parameter verwiesen wird. |
| **HC_NOREMOVE** 3 | Eine Anwendung hat die Funktion " [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) " aufgerufen, wobei "wremovemsg" auf " **PM_NOREMOVE**" festgelegt ist. Dies deutet darauf hin, dass die **Nachricht nach der** Verarbeitung der Verarbeitung nicht aus der Nachrichten Warteschlange |
| **HC_NOREMOVE** 2 | Die Hook-Prozedur muss darauf vorbereitet sein, die nächste Maus-oder Tastatur Nachricht in die **eventmsg** -Struktur zu kopieren, auf die von *LPARAM* verwiesen wird. Beim Empfang des **HC_GETNEXT** Codes muss die Hook-Prozedur die Nachricht in die-Struktur kopieren. |
| **HC_SYSMODALOFF** 5 | Ein System modales Dialogfeld wurde zerstört. Die Hook-Prozedur muss die Wiedergabe der Nachrichten fortsetzen. |
| **HC_SYSMODALON** 4 | Ein System modales Dialogfeld wird angezeigt. Bis das Dialogfeld zerstört ist, muss die Hook-Prozedur die Wiedergabe von Nachrichten abbrechen. |

### <a name="wparam"></a>wParam

Typ: **wParam**

Dieser Parameter wird nicht verwendet.

### <a name="lparam"></a>lParam

Typ: **LPARAM**

Ein Zeiger auf eine **eventmsg** -Struktur, die eine Meldung darstellt, die von der Hook-Prozedur verarbeitet wird.
Dieser Parameter ist nur gültig, wenn der *Code* Parameter **HC_GETNEXT** ist.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Damit das System vor der Verarbeitung der Nachricht warten kann, muss es sich bei dem Rückgabewert um die Zeitspanne (in Takt Einheiten) handeln, die vom System gewartet werden soll.

(Dieser Wert kann berechnet werden, indem der Unterschied zwischen den Zeit Elementen in der aktuellen und der vorherigen Eingabe Nachricht berechnet wird.)

Der Rückgabewert muss 0 (null) lauten, damit die Nachricht sofort verarbeitet werden kann. Der Rückgabewert wird nur verwendet, wenn der Hook-Code **HC_GETNEXT** ist. Andernfalls wird Sie ignoriert.

## <a name="remarks"></a>Bemerkungen

Eine **journalplaybackproc** -Hook-Prozedur sollte eine Eingabe Nachricht in den *LPARAM* -Parameter kopieren.
Die Nachricht muss zuvor mit einer **journalrecordproc** -Hook-Prozedur aufgezeichnet worden sein, die die Nachricht nicht ändern sollte.

Um dieselbe Nachricht immer wieder abzurufen, kann die Hook-Prozedur mehrmals aufgerufen werden, wobei der *Code* Parameter auf **HC_GETNEXT** festgelegt ist, ohne dass ein zwischengeschalteter Aufruf von *Code* auf **HC_SKIP** festgelegt ist.

Wenn *Code* **HC_GETNEXT** und der Rückgabewert größer als 0 (null) ist, wird das System für die durch den Rückgabewert angegebene Anzahl von Millisekunden eingestellt. Wenn das System fortgesetzt wird, wird die Hook-Prozedur erneut aufgerufen, wobei *Code* auf **HC_GETNEXT** festgelegt ist, um dieselbe Nachricht abzurufen.
Der Rückgabewert dieses neuen Aufrufes **journalplaybackproc** muss NULL sein. Andernfalls wechselt das System für die Anzahl von Millisekunden, die durch den Rückgabewert angegeben wird, wieder in den Standbymodus, rufen Sie **journalplaybackproc** erneut auf, usw.
Das System reagiert anscheinend nicht.

Im Gegensatz zu den meisten anderen globalen Hook-Prozeduren werden die Hook-Prozeduren **journalrecordproc** und **journalplaybackproc** immer im Kontext des Threads aufgerufen, der den Hook festgelegt hat.

Nachdem die Hook-Prozedur die Steuerung an das System zurückgegeben hat, wird die Nachricht weiterhin verarbeitet. Wenn *Code* **HC_SKIP** ist, muss die Hook-Prozedur die Rückgabe der nächsten aufgezeichneten Ereignis Nachricht beim nächsten-Befehl vorbereiten.

Installieren Sie die **journalplaybackproc** -Hook-Prozedur, indem Sie den [WH_JOURNALPLAYBACK](about-hooks.md) -Typ und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angeben.

Wenn der Benutzer während der Journal Wiedergabe STRG + ESC oder STRG + ALT + ENTF drückt, wird die Wiedergabe beendet, die Wiedergabe der Journal Wiedergabe Prozedur aufgehoben, und es wird eine [WM_CANCELJOURNAL](wm-canceljournal.md) Nachricht an die journalinganwendung ausgegeben.

Wenn die Hook-Prozedur eine Nachricht im Bereich zurückgibt, **WM_KEYFIRST** an **WM_KEYLAST**, gelten die folgenden Bedingungen:

* Der **paraml** -Member der **eventmsg** -Struktur gibt den Code des virtuellen Schlüssels der Taste an, die gedrückt wurde.
* Der **paramh** -Member der **eventmsg** -Struktur gibt den Scancode an.
* Es gibt keine Möglichkeit, eine Wiederholungs Anzahl anzugeben.
Das Ereignis wird immer zur Darstellung eines schlüsselereignisses verwendet.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[Eventmsg](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[Journalrecordproc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hooks](hooks.md)
