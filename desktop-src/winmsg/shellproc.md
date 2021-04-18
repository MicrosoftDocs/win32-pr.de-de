---
UID: ''
title: Shellproc-Rückruffunktion
description: Die Funktion empfängt Benachrichtigungen von shellereignissen vom System.
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
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106341295"
---
# <a name="shellproc-function"></a>Shellproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Die Funktion empfängt Benachrichtigungen von shellereignissen vom System.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Shellproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

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

Der Hook-Code.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | Der Barrierefreiheits Zustand hat sich geändert. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | Das Hauptfenster muss von der Shell aktiviert werden. |
| **HSHELL_APPCOMMAND** 12 | Der Benutzer hat ein Eingabe Ereignis abgeschlossen (z. b. eine Anwendungs Befehlsschaltfläche auf der Maus oder eine Anwendungs Befehlstaste auf der Tastatur gedrückt), und die Anwendung hat die von dieser Eingabe generierte [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) Nachricht nicht verarbeitet. Wenn die shellprozedur die [WM_COMMAND](/windows/desktop/menurc/wm-command) Nachricht behandelt, sollte Sie **CallNextHookEx** nicht aufrufen. Weitere Informationen finden Sie im Abschnitt "Rückgabewert". |
| **HSHELL_GETMINRECT** 5 | Ein Fenster wird minimiert oder maximiert. Das System benötigt die Koordinaten des minimierten Rechtecks für das Fenster. |
| **HSHELL_LANGUAGE** 8 | Die Tastatur Sprache wurde geändert, oder ein neues Tastaturlayout wurde geladen. |
| **HSHELL_REDRAW** 6 | Der Titel eines Fensters in der Taskleiste wurde neu gezeichnet. |
| **HSHELL_TASKMAN** 7 | Der Benutzer hat die Aufgabenliste ausgewählt. Eine Shellanwendung, die eine Aufgabenliste bereitstellt, sollte **true** zurückgeben, um zu verhindern, dass Windows Ihre Aufgabenliste startet. |
| **HSHELL_WINDOWACTIVATED** 4 | Die Aktivierung wurde in ein anderes Fenster der obersten Ebene (nicht im Besitz) geändert. |
| **HSHELL_WINDOWCREATED** 1 | Es wurde ein nicht eigenes Fenster der obersten Ebene erstellt. Das Fenster ist vorhanden, wenn das System diesen Hook aufruft. |
| **HSHELL_WINDOWDESTROYED** 2 | Ein Fenster der obersten Ebene, das nicht im Besitz ist, wird zerstört. Das Fenster ist weiterhin vorhanden, wenn das System diesen Hook aufruft. |
| **HSHELL_WINDOWREPLACED** 13 | Ein Fenster der obersten Ebene wird ersetzt. Das Fenster ist vorhanden, wenn das System diesen Hook aufruft. |

### <a name="wparam-in"></a>wParam [in]

Typ: **wParam**

Dieser Parameter hängt vom Wert des *nCode* -Parameters ab, wie in der folgenden Tabelle gezeigt.

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Gibt an, welche Barrierefreiheits Funktion den Zustand geändert hat. Dieser Wert ist einer der folgenden Werte: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** oder **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Gibt an, an welcher Stelle die **WM_APPCOMMAND** Nachricht ursprünglich gesendet wurde. beispielsweise das Handle für ein Fenster. Weitere Informationen finden Sie unter cmd-Parameter in **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Ein Handle für das minimierte oder maximierte Fenster. |
| **HSHELL_LANGUAGE** | Ein Handle für das Fenster. |
| **HSHELL_REDRAW** | Ein Handle für das neu erstellte Fenster. |
| **HSHELL_WINDOWACTIVATED** | Ein Handle für das aktivierte Fenster. |
| **HSHELL_WINDOWCREATED** | Ein Handle für das erstellte Fenster. |
| **HSHELL_WINDOWDESTROYED** | Ein Handle für das zerstörte Fenster. |
| **HSHELL_WINDOWREPLACED** | Ein Handle für das Fenster, das ersetzt wird. Windows 2000: nicht unterstützt. |

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Dieser Parameter hängt vom Wert des *nCode* -Parameters ab, wie in der folgenden Tabelle gezeigt.

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` der Anwendungs Befehl, der dem Eingabe Ereignis entspricht. `GET_DEVICE_LPARAM(lParam)` Gibt an, was das Eingabe Ereignis generiert hat. beispielsweise die Maus oder die Tastatur. Weitere Informationen finden Sie in der Beschreibung des Parameters " *udevice* " unter **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` hängt vom Wert von *cmd* in **WM_APPCOMMAND** ab. So kann beispielsweise angegeben werden, welche virtuellen Schlüssel beim ursprünglichen Senden der **WM_APPCOMMAND** Nachricht gedrückt gehalten wurden. Weitere Informationen finden Sie unter dem Parameter " *dwcmdflags* Description" unter **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Ein Zeiger auf eine [Rect](/previous-versions/dd162897(v=vs.85)) -Struktur. |
| **HSHELL_LANGUAGE** | Ein Handle für ein Tastaturlayout. |
| **HSHELL_MONITORCHANGED** | Ein Handle für das Fenster, das auf einen anderen Monitor verschoben wurde. |
| **HSHELL_REDRAW** | Der Wert ist " **true** ", wenn das Fenster blinkt, andernfalls " **false** ". |
| **HSHELL_WINDOWACTIVATED** | Der Wert ist "true", wenn sich das Fenster im Vollbildmodus befindet, andernfalls " **false** ". |
| **HSHELL_WINDOWREPLACED** | Ein Handle für das neue Fenster. Windows 2000: nicht unterstützt. |

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Der Rückgabewert sollte NULL sein, es sei denn, der Wert von nCode ist **HSHELL_APPCOMMAND** , und die shellprozedur verarbeitet die **WM_COMMAND** -Nachricht.
In diesem Fall sollte die Rückgabe nicht NULL sein.

## <a name="remarks"></a>Bemerkungen

Installieren Sie diese Hook-Prozedur, indem Sie den [WH_SHELL](about-hooks.md) Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angeben.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Hooks](hooks.md)
