---
title: CLASS-Anweisung
description: Definiert die Klasse des Dialogfelds.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- CLASS-Anweisungsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a71485603944dc8b7eaf1a3a773051096776e6538aecdd8fb01396a3f0ea5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734656"
---
# <a name="class-statement"></a>CLASS-Anweisung

Definiert die Klasse des Dialogfelds.

Die **CLASS-Anweisung** wird im optionalen Abschnitt vor dem Main einer [**DIALOG-Anweisung**](dialog-resource.md) angezeigt. Wenn keine Klasse angegeben wird, wird die Standarddialogklasse verwendet.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Klasse*
</dt> <dd>

Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge in doppelten Anführungszeichen (), die die Klasse des Dialogfelds identifiziert. Wenn die Fensterprozedur für die -Klasse keine an sie gesendete Nachricht verarbeitet, muss sie die [**DefDlgProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) aufrufen, um sicherzustellen, dass alle Nachrichten ordnungsgemäß für das Dialogfeld behandelt werden. Eine private Klasse kann **DefDlgProc als** Standardfensterprozedur verwenden. Die -Klasse muss mit dem **cbWndExtra-Member** der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) registriert werden, die auf **DLGWINDOWEXTRA festgelegt ist.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CLASS-Anweisung** sollte nur in Sonderfällen verwendet werden, da sie die normale Verarbeitung eines Dialogfelds überschreibt. Die **CLASS-Anweisung** konvertiert ein Dialogfeld in ein Fenster der angegebenen Klasse. Je nach Klasse kann dies zu unerwünschten Ergebnissen führen. Verwenden Sie nicht die neu definierten Steuerelementklassennamen mit dieser Anweisung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **CLASS-Anweisung** veranschaulicht:

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DIALOG**](dialog-resource.md)
</dt> </dl>

 

 