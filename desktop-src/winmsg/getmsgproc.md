---
UID: ''
title: GetMsgProc-Rückruffunktion
description: Das System ruft diese Funktion auf, wenn eine Nachrichtenfunktion eine Nachricht aus einer Anwendungsnachrichtenwarteschlange erhält.
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
ms.openlocfilehash: e5c51f2abe8b3660ae40bae05c13428e0622fd4d5c4b8020fea8caa924a35681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200792"
---
# <a name="getmsgproc-function"></a>GetMsgProc-Funktion

## <a name="-description"></a>-description

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion verwendet](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) wird. Das System ruft diese Funktion auf, wenn die [GetMessage-](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [PeekMessage-Funktion](/windows/desktop/api/winuser/nf-winuser-peekmessagew) eine Nachricht aus einer Anwendungsnachrichtenwarteschlange abgerufen hat.
Bevor die abgerufene Nachricht an den Aufrufer zurückgibt, übergibt das System die Nachricht an die Hookprozedur.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**GetMsgProc ist** ein Platzhalter für den anwendungs- oder bibliotheksdefinierten Funktionsnamen.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-parameters

### <a name="code-in"></a>Code [in]

Typ: **int**

Gibt an, ob die Hookprozedur die Nachricht verarbeiten muss.
Wenn  Code **HC_ACTION** ist, muss die Hookprozedur die Nachricht verarbeiten.
Wenn *der* Code kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

### <a name="wparam-in"></a>wParam [in]

Typ: **WPARAM**

Gibt an, ob die Nachricht aus der Warteschlange entfernt wurde.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | Die Nachricht wurde nicht aus der Warteschlange entfernt. (Eine Anwendung namens **PeekMessage-Funktion,** die das **PM_NOREMOVE** an.) |
| **PM_REMOVE** 0x0001 | Die Nachricht wurde aus der Warteschlange entfernt. (Eine Anwendung mit dem **Namen GetMessage,** oder sie hat die **PeekMessage-Funktion** aufgerufen und das PM_REMOVE **angegeben.)**|

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [MSG-Struktur,](/windows/desktop/api/winuser/ns-winuser-msg) die Details zur Nachricht enthält.

## <a name="-returns"></a>-returns

Wenn *der Code* kleiner als 0 (null) ist, muss die Hookprozedur den von [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)zurückgegebenen Wert zurückgeben.

Wenn *der* Code größer oder gleich 0 (null) ist, wird dringend empfohlen, **CallNextHookEx** auf aufruft und den zurückgegebenen Wert zurückgibt. Andernfalls erhalten andere [](about-hooks.md) Anwendungen, die WH_GETMESSAGE Hooks installiert haben, keine Hookbenachrichtigungen und verhalten sich möglicherweise falsch.
Wenn die Hookprozedur **CallNextHookEx nicht aufruft,** sollte der Rückgabewert 0 (null) sein.

## <a name="-remarks"></a>-remarks

Die **Hookprozedur GetMsgProc** kann die Nachricht überprüfen oder ändern.
Nachdem die Hookprozedur die Steuerung an das System zurückgegeben hat, gibt die **GetMessage-** oder **PeekMessage-Funktion** die Nachricht zusammen mit allen Änderungen an die Anwendung zurück, die sie ursprünglich aufgerufen hat.

Eine Anwendung installiert diese Hookprozedur, indem WH_GETMESSAGE Hooktyp und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** angeben. 

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[Msg](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)
