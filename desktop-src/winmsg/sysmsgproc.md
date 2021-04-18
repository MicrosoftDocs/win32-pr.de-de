---
UID: ''
title: Sysmsgproc-Rückruffunktion
description: Das System ruft diese Funktion auf, nachdem ein Eingabe Ereignis in einem Dialogfeld, einem Meldungs Feld, einem Menü oder einer Scrollleiste auftritt. | Sysmsgproc-Rückruffunktion
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
ms.openlocfilehash: 0d5c7fc116b74dada141e88116ba67209da4a103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365282"
---
# <a name="sysmsgproc-function"></a>Sysmsgproc-Funktion

## <a name="description"></a>BESCHREIBUNG

Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.
Das System ruft diese Funktion auf, nachdem ein Eingabe Ereignis in einem Dialogfeld, einem Meldungs Feld, einem Menü oder einer Scrollleiste aufgetreten ist, aber bevor die vom Eingabe Ereignis generierte Meldung verarbeitet wird.
Die-Funktion kann Meldungen für beliebige Dialogfelder, ein Meldungs Feld, ein Menü oder eine Bild Lauf Leiste im System überwachen.

Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.
**Sysmsgproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.

```cpp
LRESULT CALLBACK SysMsgProc(
  _In_ int    nCode,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

### <a name="ncode-in"></a>nCode [in]

Typ: **int**

Der Typ des Eingabe Ereignisses, von dem die Meldung generiert wurde.
Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.
Dieser Parameter kann einen der folgenden Werte annehmen.

| Wert | Bedeutung |
|-------|---------|
| **MSGF_DIALOGBOX** 0 | Das Eingabe Ereignis ist in einem Meldungs Feld oder Dialogfeld aufgetreten. |
| **MSGF_MENU** 2 | Das Eingabe Ereignis ist in einem Menü aufgetreten. |
| **MSGF_SCROLLBAR** 5 | Das Eingabe Ereignis ist in einer Bild Lauf Leiste aufgetreten. |

### <a name="wparam"></a>wParam

Typ: **wParam**

Dieser Parameter wird nicht verwendet.

### <a name="lparam-in"></a>LParam [in]

Typ: **LPARAM**

Ein Zeiger auf eine [Nachrichten Nachrichten](/windows/desktop/api/winuser/ns-winuser-msg) Struktur.

## <a name="returns"></a>Gibt zurück

Typ: **LRESULT**

Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.

Wenn *nCode* größer als oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_SYSMSGFILTER](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.
Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an die Zielfenster Prozedur übergibt.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_SYSMSGFILTER** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.

## <a name="see-also"></a>Siehe auch

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[Meldung](/windows/desktop/api/winuser/ns-winuser-msg)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)
