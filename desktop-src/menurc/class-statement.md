---
title: Class-Anweisung
description: Definiert die Klasse des Dialog Felds.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Klassen Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948674"
---
# <a name="class-statement"></a>Class-Anweisung

Definiert die Klasse des Dialog Felds.

Die **Class** -Anweisung wird im optionalen Abschnitt vor dem Hauptabschnitt der [**Dialog**](dialog-resource.md) Feld Anweisung angezeigt. Wenn keine Klasse angegeben wird, wird die Standard Dialogklasse verwendet.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*klassi*
</dt> <dd>

Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die die Klasse des Dialog Felds angibt. Wenn die Fenster Prozedur für die Klasse keine an Sie gesendete Nachricht verarbeitet, muss Sie die Funktion [**defdlgproc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) aufgerufen werden, um sicherzustellen, dass alle Nachrichten ordnungsgemäß für das Dialogfeld verarbeitet werden. Eine private Klasse kann **defdlgproc** als Standardfenster Prozedur verwenden. Die Klasse muss beim **CbWndExtra** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur, die auf **dlgwindowextra** festgelegt ist, registriert werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Class** -Anweisung sollte nur in besonderen Fällen verwendet werden, da Sie die normale Verarbeitung eines Dialog Felds überschreibt. Die **Class** -Anweisung konvertiert ein Dialogfeld in ein Fenster der angegebenen Klasse. abhängig von der-Klasse kann dies zu unerwünschten Ergebnissen führen. Verwenden Sie die neu definierten Steuerelement Klassennamen nicht mit dieser Anweisung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Class** -Anweisung veranschaulicht:

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Defdlgproc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**Dialog**](dialog-resource.md)
</dt> </dl>

 

 