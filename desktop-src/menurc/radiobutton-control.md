---
title: RADIOBUTTON-Steuerelement
description: Definiert ein Optionsfeld-Steuerelement.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- RADIOBUTTON-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b01d6b2313ec4b881f182fd4a4ca34cf5bbf713dca9f329173d1817132606d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952250"
---
# <a name="radiobutton-control"></a>RADIOBUTTON-Steuerelement

Definiert ein Optionsfeld-Steuerelement. Das Steuerelement ist ein kleiner Kreis, neben dem der text angezeigt wird, in der Regel rechts davon. Das Steuerelement hebt den Kreis hervor und sendet eine Nachricht an das übergeordnete Fenster, wenn der Benutzer die Schaltfläche auswählt. Das -Steuerelement entfernt die Hervorhebung und sendet eine Meldung, wenn die Schaltfläche das nächste Mal ausgewählt wird.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Stile für das Optionsfeld, bei dem es sich um eine Kombination aus BUTTON-Klassenstilen und den folgenden Stilen sein kann: **WS \_ TABSTOP,** **WS \_ DISABLED** und **WS \_ GROUP**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **RADIOBUTTON-Anweisung** veranschaulicht:

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Optionsfelder](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 