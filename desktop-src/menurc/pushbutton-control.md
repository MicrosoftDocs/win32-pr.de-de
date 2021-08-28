---
title: PUSHBUTTON-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Schaltflächen-Steuerelement. Das -Steuerelement ist ein rechteckiges Rechteck mit dem angegebenen Text. Der Text wird im -Steuerelement zentriert. Das Steuerelement sendet eine Nachricht an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- PUSHBUTTON-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24db89c986f3f6d466f1710bc18420f9da9eec3348eada10e95582a882fe25e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777000"
---
# <a name="pushbutton-control"></a>PUSHBUTTON-Steuerelement

Definiert ein Schaltflächen-Steuerelement. Das -Steuerelement ist ein rechteckiges Rechteck mit dem angegebenen Text. Der Text wird im -Steuerelement zentriert. Das Steuerelement sendet eine Nachricht an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Stile für den Pushbutton, bei dem es sich um eine Kombination aus **dem BS \_ PUSHBUTTON-Stil** und den folgenden Stilen sein kann: **WS \_ TABSTOP,** **WS \_ DISABLED** und **WS \_ GROUP**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **PUSHBUTTON-Anweisung** veranschaulicht:

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Pushschaltflächen](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 