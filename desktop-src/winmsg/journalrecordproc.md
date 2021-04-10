---
UID: ''
title: Journalrecordproc-Rückruffunktion
description: Die Funktion zeichnet Meldungen auf, die das System aus der System Meldungs Warteschlange entfernt.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "103948535"
---
# <a name="journalrecordproc-function"></a>Journalrecordproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Die Funktion zeichnet Meldungen auf, die das System aus der System Meldungs Warteschlange entfernt.
Später kann eine Anwendung eine [journalplaybackproc](journalplaybackproc.md) -Hook-Prozedur verwenden, um die Nachrichten wiederzugeben.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Journalrecordproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="code-in"></a>Code [in]

Typ: **int**

Gibt an, wie die Nachricht verarbeitet werden soll.
Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Der *LPARAM* -Parameter ist ein Zeiger auf eine [eventmsg](/windows/desktop/api/winuser/ns-winuser-eventmsg) -Struktur, die Informationen zu einer Nachricht enthält, die aus der System Warteschlange entfernt wurde. Die Hook-Prozedur muss den Inhalt der Struktur aufzeichnen, indem Sie Sie in einen Puffer oder eine Datei kopieren. |
| **HC_SYSMODALOFF** 5 | Ein System modales Dialogfeld wurde zerstört. Die Hook-Prozedur muss die Aufzeichnung fortsetzen. |
| **HC_SYSMODALON** 4 | Ein System modales Dialogfeld wird angezeigt. Die Hook-Prozedur muss die Aufzeichnung anhalten, bis das Dialogfeld zerstört ist. |

### <a name="wparam"></a>wParam

Typ: **wParam**

Dieser Parameter wird nicht verwendet.

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine **eventmsg** -Struktur, die die zu zeichnenden Meldung enthält.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Eine **journalrecordproc** -Hook-Prozedur muss die Nachrichten kopieren, aber nicht ändern.
Nachdem die Hook-Prozedur die Steuerung an das System zurückgegeben hat, wird die Nachricht weiterhin verarbeitet.

Installieren Sie die **journalrecordproc** -Hook-Prozedur, indem Sie den [WH_JOURNALRECORD](about-hooks.md) -Typ und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angeben.

Eine **journalrecordproc** -Hook-Prozedur muss nicht in einer Dynamic Link Library Leben.
Eine **journalrecordproc** -Hook-Prozedur kann in der Anwendung selbst leben.

Im Gegensatz zu den meisten anderen globalen Hook-Prozeduren werden die Hook-Prozeduren **journalrecordproc** und [journalplaybackproc](journalplaybackproc.md) immer im Kontext des Threads aufgerufen, der den Hook festgelegt hat.

Eine Anwendung, die eine **journalrecordproc** -Hook-Prozedur installiert hat, sollte den [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) Code des virtuellen Schlüssels überwachen (der in den meisten Tastaturen als STRG + unt-Schlüsselkombination implementiert ist).
Dieser virtuelle Schlüsselcode sollte von der Anwendung als Signal interpretiert werden, dass der Benutzer die Journal Aufzeichnung anhalten möchte.
Die Anwendung sollte Antworten, indem Sie die Aufzeichnungs Sequenz beendet und die **journalrecordproc** -Hook-Prozedur entfernt.
Das Entfernen ist wichtig.
Dadurch wird verhindert, dass eine Journal Anwendung das System sperrt, indem es in einer Hook-Prozedur hängt.

Diese Rolle als Signal zum Anhalten der Journl-Aufzeichnung bedeutet, dass die Tastenkombination STRG + UNTBR nicht selbst aufgezeichnet werden kann.
Da die Tastenkombination STRG + C keine Rolle spielt, kann Sie aufgezeichnet werden.
Es gibt zwei weitere Tastenkombinationen, die nicht aufgezeichnet werden können: STRG + ESC und STRG + ALT + ENTF.
Diese beiden Tastenkombinationen bewirken, dass das System alle journalingaktivitäten beendet (aufzeichnen oder Wiedergabe), alle journalhooks entfernt und eine [WM_CANCELJOURNAL](wm-canceljournal.md) Nachricht in der Journal Anwendung sendet.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[Eventmsg](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[Journalplaybackproc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hooks](hooks.md)
