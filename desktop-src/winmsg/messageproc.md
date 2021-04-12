---
UID: ''
title: MessageProc-Rückruffunktion
description: Das System ruft diese Funktion auf, nachdem ein Eingabe Ereignis in einem Dialogfeld, einem Meldungs Feld, einem Menü oder einer Scrollleiste auftritt. | MessageProc-Rückruffunktion
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
ms.openlocfilehash: 00a1d1c52d50d0d9a028829181c886a813112a15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353569"
---
# <a name="messageproc-function"></a>MessageProc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Das System ruft diese Funktion auf, nachdem ein Eingabe Ereignis in einem Dialogfeld, einem Meldungs Feld, einem Menü oder einer Scrollleiste aufgetreten ist, aber bevor die vom Eingabe Ereignis generierte Meldung verarbeitet wird.
Die Hook-Prozedur kann Meldungen für ein Dialogfeld, ein Meldungs Feld, ein Menü oder eine Bild Lauf Leiste überwachen, die von einer bestimmten Anwendung oder von allen Anwendungen erstellt wurde.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**MessageProc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

```cpp
LRESULT CALLBACK MessageProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="code-in"></a>Code [in]

Typ: **int**

Der Typ des Eingabe Ereignisses, von dem die Meldung generiert wurde.
Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben, ohne die Verarbeitung zu verarbeiten und den von **CallNextHookEx** zurückgegebenen Wert zurückzugeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | Das Eingabe Ereignis ist aufgetreten, während die dynamischer Datenaustausch Management Library (Ddeml) darauf wartete, dass eine synchrone Transaktion abgeschlossen wird. Weitere Informationen zu DDEML finden Sie unter [dynamischer Datenaustausch-Verwaltungs Bibliothek](../dataxchg/dynamic-data-exchange-management-library.md). |
| **MSGF_DIALOGBOX** 0 | Das Eingabe Ereignis ist in einem Meldungs Feld oder Dialogfeld aufgetreten. |
| **MSGF_MENU** 2 | Das Eingabe Ereignis ist in einem Menü aufgetreten. |
| **MSGF_SCROLLBAR** 5 | Das Eingabe Ereignis ist in einer Bild Lauf Leiste aufgetreten. |

### <a name="wparam"></a>wParam

Typ: **wParam**

Dieser Parameter wird nicht verwendet.

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [msg](/windows/win32/api/winuser/ns-winuser-msg) -Struktur.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *Code* größer oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_MSGFILTER](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.
Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hook-Kette oder der Zielfenster Prozedur übergibt.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_MSGFILTER** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.

Wenn eine Anwendung, die die Ddeml verwendet und synchrone Transaktionen ausführt, Nachrichten verarbeiten muss, bevor Sie gesendet werden, muss der **WH_MSGFILTER** Hook verwendet werden.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Meldung](/windows/win32/api/winuser/ns-winuser-msg)

[Hooks](hooks.md)
