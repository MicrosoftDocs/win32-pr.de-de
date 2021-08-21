---
UID: ''
title: JournalRecordProc-Rückruffunktion
description: Die Funktion zeichnet Meldungen auf, die das System aus der Systemnachrichtenwarteschlange entfernt.
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
ms.openlocfilehash: cc5e1bdbd99b234b347d0b9c10caa7125aead9b68138472e125c8e2a11180609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437117"
---
# <a name="journalrecordproc-function"></a>JournalRecordProc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion verwendet](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) wird.
Die Funktion zeichnet Meldungen auf, die das System aus der Systemnachrichtenwarteschlange entfernt.
Später kann eine Anwendung eine [JournalPlaybackProc-Hookprozedur](journalplaybackproc.md) verwenden, um die Nachrichten wiederzuverspielen.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**JournalRecordProc ist** ein Platzhalter für den anwendungs- oder bibliotheksdefinierten Funktionsnamen.

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

Gibt an, wie die Nachricht zu verarbeiten ist.
Wenn *der* Code kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HC_ACTION** 0 | Der *lParam-Parameter* ist ein Zeiger auf eine [EVENTMSG-Struktur,](/windows/desktop/api/winuser/ns-winuser-eventmsg) die Informationen zu einer Nachricht enthält, die aus der Systemwarteschlange entfernt wurde. Die Hookprozedur muss den Inhalt der -Struktur aufzeichnen, indem sie sie in einen Puffer oder eine Datei kopiert. |
| **HC_SYSMODALOFF** 5 | Ein system modales Dialogfeld wurde zerstört. Die Hookprozedur muss die Aufzeichnung fortsetzen. |
| **HC_SYSMODALON** 4 | Ein system modales Dialogfeld wird angezeigt. Bis das Dialogfeld zerstört wird, muss die Hookprozedur die Aufzeichnung beenden. |

### <a name="wparam"></a>wParam

Typ: **WPARAM**

Dieser Parameter wird nicht verwendet.

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine **EVENTMSG-Struktur,** die die zu notierende Nachricht enthält.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Eine **JournalRecordProc-Hookprozedur** muss die Nachrichten kopieren, aber nicht ändern.
Nachdem die Hookprozedur die Steuerung an das System zurückgegeben hat, wird die Nachricht weiterhin verarbeitet.

Installieren Sie die Hookprozedur **JournalRecordProc,** indem Sie den WH_JOURNALRECORD-Typ und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angeben. [](about-hooks.md)

Eine **JournalRecordProc-Hookprozedur** muss nicht in einer Dynamic Link Library gespeichert werden.
Eine **JournalRecordProc-Hookprozedur** kann in der Anwendung selbst verwendet werden.

Im Gegensatz zu den meisten anderen globalen Hookprozeduren werden die Hookprozeduren **JournalRecordProc** und [JournalPlaybackProc](journalplaybackproc.md) immer im Kontext des Threads aufgerufen, der den Hook festlegen.

Eine Anwendung, die eine **JournalRecordProc-Hookprozedur** installiert hat, sollte auf den virtuellen [VK_CANCEL-Schlüsselcode](/windows/desktop/inputdev/virtual-key-codes) achten (der auf den meisten Tastaturen als TASTENKOMBINATION STRG+BREAK implementiert ist).
Dieser Virtuelle Schlüsselcode sollte von der Anwendung als Signal interpretiert werden, dass der Benutzer die Journalaufzeichnung beenden möchte.
Die Anwendung sollte reagieren, indem sie die Aufzeichnungssequenz beendet und die **Hookprozedur JournalRecordProc** entfernt.
Das Entfernen ist wichtig.
Sie verhindert, dass eine Journalanwendung das System sperrt, indem sie in einer Hookprozedur hängt.

Diese Rolle als Signal zum Beenden der Journl-Aufzeichnung bedeutet, dass eine TASTENKOMBINATION STRG+BREAK nicht selbst aufgezeichnet werden kann.
Da die Tastenkombination STRG+C keine rolle wie ein Journalsignal hat, kann sie aufgezeichnet werden.
Es gibt zwei weitere Tastenkombinationen, die nicht aufgezeichnet werden können: STRG+ESC und STRG+ALT+ENTF.
Diese beiden Tastenkombinationen bewirken, dass das System alle Journalingaktivitäten (Aufzeichnung oder Wiedergabe) stoppt, alle [Journalinghooks](wm-canceljournal.md) entfernt und eine WM_CANCELJOURNAL an die Journalanwendung übermittelt.

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hooks](hooks.md)
