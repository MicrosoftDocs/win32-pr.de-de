---
UID: ''
title: MessageProc-Rückruffunktion
description: Das System ruft diese Funktion auf, nachdem ein Eingabeereignis in einem Dialogfeld, Meldungsfeld, Menü oder einer Bildlaufleiste auftritt. | MessageProc-Rückruffunktion
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
ms.openlocfilehash: 6da307d00c9291ab8c27b97c5012c9887b5c12fcbc541beb5a9b7e8c176ec5a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200782"
---
# <a name="messageproc-function"></a>MessageProc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine anwendungs- oder bibliotheksdefinierte Rückruffunktion, die mit der [SetWindowsHookEx-Funktion verwendet](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) wird.
Das System ruft diese Funktion auf, nachdem ein Eingabeereignis in einem Dialogfeld, Meldungsfeld, Menü oder einer Bildlaufleiste auftritt, aber bevor die vom Eingabeereignis generierte Nachricht verarbeitet wird.
Die Hookprozedur kann Nachrichten für ein Dialogfeld, ein Meldungsfeld, ein Menü oder eine Bildlaufleiste überwachen, die von einer bestimmten Anwendung oder allen Anwendungen erstellt wurden.

Der **HOOKPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion.
**MessageProc ist** ein Platzhalter für den anwendungs- oder bibliotheksdefinierten Funktionsnamen.

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

Der Typ des Eingabeereigniss, das die Nachricht generiert hat.
Wenn *der* Code kleiner als 0 (null) ist, muss die Hookprozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx-Funktion](/windows/desktop/api/winuser/nf-winuser-callnexthookex) übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | Das Eingabeereignis ist aufgetreten, während die dynamische Daten Exchange Management Library (DDEML) auf den Abschluss einer synchronen Transaktion wartete. Weitere Informationen zu DDEML finden Sie unter [dynamische Daten Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md). |
| **MSGF_DIALOGBOX** 0 | Das Eingabeereignis ist in einem Meldungsfeld oder Dialogfeld aufgetreten. |
| **MSGF_MENU** 2 | Das Eingabeereignis ist in einem Menü aufgetreten. |
| **MSGF_SCROLLBAR** 5 | Das Eingabeereignis ist in einer Bildlaufleiste aufgetreten. |

### <a name="wparam"></a>wParam

Typ: **WPARAM**

Dieser Parameter wird nicht verwendet.

### <a name="lparam-in"></a>lParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [MSG-Struktur.](/windows/win32/api/winuser/ns-winuser-msg)

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *der Code* kleiner als 0 (null) ist, muss die Hookprozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *code* größer oder gleich 0 (null) ist und die Hookprozedur die Nachricht nicht verarbeiten konnte, wird dringend empfohlen, **CallNextHookEx** auf aufruft und den zurückgegebenen Wert zurückgibt. Andernfalls erhalten andere Anwendungen, die WH_MSGFILTER [Hooks](about-hooks.md) installiert haben, keine Hookbenachrichtigungen und verhalten sich möglicherweise falsch.
Wenn die Hookprozedur die Nachricht verarbeitet hat, wird möglicherweise ein Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hookkette oder die Zielfensterprozedur übergehen kann.

## <a name="remarks"></a>Hinweise

Eine Anwendung installiert die Hookprozedur, indem sie den Hooktyp WH_MSGFILTER und einen Zeiger auf die Hookprozedur in einem Aufruf der **SetWindowsHookEx-Funktion** an. 

Wenn eine Anwendung, die die DDEML verwendet und synchrone Transaktionen ausführt, Nachrichten verarbeiten muss, bevor sie **gesendet werden,** muss sie den WH_MSGFILTER verwenden.

## <a name="see-also"></a>Weitere Informationen

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Msg](/windows/win32/api/winuser/ns-winuser-msg)

[Hooks](hooks.md)
