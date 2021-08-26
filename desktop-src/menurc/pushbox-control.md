---
title: PUSHBOX-Steuerelement
description: Definiert ein Pushbox-Steuerelement, das mit einem PUSHBUTTON identisch ist, mit dem Unterschied, dass keine Schaltflächenfläche oder kein Frame angezeigt wird. wird nur der Text angezeigt.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- MENÜS und andere Ressourcen des PUSHBOX-Steuerelements
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06135aad813141e15bede8364a71e8fbc3016c7cb79afe0085bb6bc7bbcb2d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952370"
---
# <a name="pushbox-control"></a>PUSHBOX-Steuerelement

Definiert ein Pushbox-Steuerelement, das mit einem [**PUSHBUTTON**](pushbutton-control.md)identisch ist, mit der Ausnahme, dass keine Schaltflächenfläche oder kein Frame angezeigt wird. wird nur der Text angezeigt.

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Stile für die Pushbox, die eine Kombination aus dem **\_ BS-PUSHBOX-Stil** und den folgenden Stilen sein können: **WS \_ TABSTOP**, **WS \_ DISABLED** und **WS \_ GROUP**.

Wenn Sie keinen Stil angeben, lautet der Standardstil `BS_PUSHBOX | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schaltflächen drücken](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**Pushbutton**](pushbutton-control.md)
</dt> </dl>

 

 




