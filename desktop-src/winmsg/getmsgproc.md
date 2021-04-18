---
UID: ''
title: Getmsgproc-Rückruffunktion
description: Das System ruft diese Funktion auf, wenn eine Nachrichten Funktion eine Nachricht aus einer Anwendungs Nachrichten Warteschlange abruft.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "106344154"
---
# <a name="getmsgproc-function"></a>Getmsgproc-Funktion

## <a name="-description"></a>-Beschreibung

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird. Das System ruft diese Funktion immer dann auf, wenn die [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) -Funktion oder die [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) -Funktion eine Nachricht aus einer Anwendungs Nachrichten Warteschlange abgerufen hat.
Bevor die abgerufene Nachricht an den Aufrufer zurückgegeben wird, übergibt das System die Nachricht an die Hook-Prozedur.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Getmsgproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-Parameter

### <a name="code-in"></a>Code [in]

Typ: **int**

Gibt an, ob die Hook-Prozedur die Nachricht verarbeiten muss.
Wenn *Code* **HC_ACTION** ist, muss die Hook-Prozedur die Nachricht verarbeiten.
Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

### <a name="wparam-in"></a>wParam [in]

Typ: **wParam**

Gibt an, ob die Nachricht aus der Warteschlange entfernt wurde.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | Die Nachricht wurde nicht aus der Warteschlange entfernt. (Eine Anwendung, die die Funktion " **Peer Message** " genannt wird und das **PM_NOREMOVE** Flag angibt.) |
| **PM_REMOVE** 0x0001 | Die Nachricht wurde aus der Warteschlange entfernt. (Eine Anwendung namens **GetMessage** oder die Funktion "  **Peer Message** ", die das **PM_REMOVE** -Flag angibt.)|

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [msg](/windows/desktop/api/winuser/ns-winuser-msg) -Struktur, die Details über die Nachricht enthält.

## <a name="-returns"></a>-Gibt zurück

Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur den von [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)zurückgegebenen Wert zurückgeben.

Wenn *Code* größer als oder gleich 0 (null) ist, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_GETMESSAGE](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.
Wenn die Hook-Prozedur **CallNextHookEx** nicht aufruft, sollte der Rückgabewert 0 (null) lauten.

## <a name="-remarks"></a>-Hinweise

Die **getmsgproc** -Hook-Prozedur kann die Nachricht überprüfen oder ändern.
Nachdem die Hook-Prozedur die Steuerung an das System zurückgegeben hat, gibt die **GetMessage** -Funktion oder die **Peer Message** -Funktion die Nachricht zusammen mit allen Änderungen an die Anwendung zurück, die Sie ursprünglich aufgerufen hat.

Eine Anwendung installiert diese Hook-Prozedur, indem Sie den **WH_GETMESSAGE** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[Meldung](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)
