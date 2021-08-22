---
UID: ''
title: ShellProc-Rückruffunktion
description: Die Funktion empfängt Benachrichtigungen über Shell-Ereignisse vom System.
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
ms.openlocfilehash: 3776748994b44b3a870fd4689fa9f4019bff99ae8d6f7dd7b13edbf2c98054d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449100"
---
# <a name="shellproc-function"></a>ShellProc-Funktion

## <a name="description"></a>Beschreibung

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) verwendet wird.
Die Funktion empfängt Benachrichtigungen über Shell-Ereignisse vom System.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**ShellProc** ist ein Platzhalter für den anwendungs- oder bibliotheksdefinierte Funktionsnamen.

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="ncode-in"></a>nCode [in]

Typ: **int**

Der Hookcode.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und sollte den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | Der Zustand der Barrierefreiheit wurde geändert. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | Die Shell sollte ihr Hauptfenster aktivieren. |
| **HSHELL_APPCOMMAND** 12 | Der Benutzer hat ein Eingabeereignis abgeschlossen (z. B. eine Anwendungsbefehlsschaltfläche mit der Maus oder eine Anwendungsbefehlstaste auf der Tastatur), und die Anwendung hat die von dieser Eingabe generierte [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) Meldung nicht verarbeitet. Wenn die Shell-Prozedur die [WM_COMMAND](/windows/desktop/menurc/wm-command) Meldung verarbeitet, sollte **callNextHookEx** nicht aufgerufen werden. Weitere Informationen finden Sie im Abschnitt Rückgabewert. |
| **HSHELL_GETMINRECT** 5 | Ein Fenster wird minimiert oder maximiert. Das System benötigt die Koordinaten des minimierten Rechtecks für das Fenster. |
| **HSHELL_LANGUAGE** 8 | Die Tastatursprache wurde geändert, oder es wurde ein neues Tastaturlayout geladen. |
| **HSHELL_REDRAW** 6 | Der Titel eines Fensters in der Taskleiste wurde neu gezeichnet. |
| **HSHELL_TASKMAN** 7 | Der Benutzer hat die Aufgabenliste ausgewählt. Eine Shellanwendung, die eine Aufgabenliste bereitstellt, sollte **TRUE** zurückgeben, um zu verhindern, dass Windows ihre Aufgabenliste startet. |
| **HSHELL_WINDOWACTIVATED** 4 | Die Aktivierung wurde in ein anderes Fenster der obersten Ebene ohne Besitzer geändert. |
| **HSHELL_WINDOWCREATED** 1 | Es wurde ein Fenster der obersten Ebene ohne Eigentümer erstellt. Das Fenster ist vorhanden, wenn das System diesen Hook aufruft. |
| **HSHELL_WINDOWDESTROYED** 2 | Ein fensterloses Fenster der obersten Ebene wird zerstört. Das Fenster ist weiterhin vorhanden, wenn das System diesen Hook aufruft. |
| **HSHELL_WINDOWREPLACED** 13 | Ein Fenster der obersten Ebene wird ersetzt. Das Fenster ist vorhanden, wenn das System diesen Hook aufruft. |

### <a name="wparam-in"></a>wParam [in]

Typ: **WPARAM**

Dieser Parameter hängt vom Wert des *nCode-Parameters* ab, wie in der folgenden Tabelle gezeigt.

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Gibt an, welches Barrierefreiheitsfeature den Zustand geändert hat. Dieser Wert ist einer der folgenden: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** oder **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Gibt an, wo die **WM_APPCOMMAND** Nachricht ursprünglich gesendet wurde. z. B. das Handle für ein Fenster. Weitere Informationen finden Sie unter cmd-Parameter in **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Ein Handle für das minimierte oder maximierte Fenster. |
| **HSHELL_LANGUAGE** | Ein Handle für das Fenster. |
| **HSHELL_REDRAW** | Ein Handle für das neu gezeichnete Fenster. |
| **HSHELL_WINDOWACTIVATED** | Ein Handle für das aktivierte Fenster. |
| **HSHELL_WINDOWCREATED** | Ein Handle für das erstellte Fenster. |
| **HSHELL_WINDOWDESTROYED** | Ein Handle für das zerstörte Fenster. |
| **HSHELL_WINDOWREPLACED** | Ein Handle für das Fenster, das ersetzt wird. Windows 2000: Nicht unterstützt. |

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Dieser Parameter hängt vom Wert des *nCode-Parameters* ab, wie in der folgenden Tabelle gezeigt.

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` ist der Anwendungsbefehl, der dem Eingabeereignis entspricht. `GET_DEVICE_LPARAM(lParam)` gibt an, was das Eingabeereignis generiert hat. z. B. die Maus oder Tastatur. Weitere Informationen finden Sie in der Beschreibung des *uDevice-Parameters* unter **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` hängt vom Wert von *cmd* in **WM_APPCOMMAND** ab. Beispielsweise kann dies darauf hinweisen, welche virtuellen Schlüssel beim ursprünglichen Senden der **WM_APPCOMMAND** Nachricht gedrückt gehalten wurden. Weitere Informationen finden Sie im *dwCmdFlags* description-Parameter unter **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Ein Zeiger auf eine [RECT-Struktur.](/previous-versions/dd162897(v=vs.85)) |
| **HSHELL_LANGUAGE** | Ein Handle für ein Tastaturlayout. |
| **HSHELL_MONITORCHANGED** | Ein Handle für das Fenster, das auf einen anderen Monitor verschoben wurde. |
| **HSHELL_REDRAW** | Der Wert ist **TRUE,** wenn das Fenster blinkt, **andernfalls FALSE.** |
| **HSHELL_WINDOWACTIVATED** | Der Wert ist TRUE, wenn sich das Fenster im Vollbildmodus befindet, andernfalls **FALSE.** |
| **HSHELL_WINDOWREPLACED** | Ein Handle für das neue Fenster. Windows 2000: Nicht unterstützt. |

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Der Rückgabewert sollte 0 (null) sein, es sei denn, der Wert von nCode ist **HSHELL_APPCOMMAND,** und die Shellprozedur verarbeitet die **WM_COMMAND** Nachricht.
In diesem Fall sollte die Rückgabe ungleich 0 (null) sein.

## <a name="remarks"></a>Hinweise

Installieren Sie diese Hookprozedur, indem Sie den [WH_SHELL](about-hooks.md) Hooktyp und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angeben.

## <a name="see-also"></a>Weitere Informationen:

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Hooks](hooks.md)
