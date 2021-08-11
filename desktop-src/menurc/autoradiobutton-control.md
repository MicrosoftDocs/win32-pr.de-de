---
title: AUTOGRAMMBUTTON-Steuerelement
description: Definiert ein automatisches Optionsfeld-Steuerelement. Dieses Steuerelement führt automatisch den gegenseitigen Ausschluss mit den anderen AUTOGRAMMBUTTON-Steuerelementen in derselben Gruppe aus. Wenn die Schaltfläche ausgewählt wird, wird die Anwendung per \_ BN-KLICK benachrichtigt.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- AUTOGRAMMBUTTON-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8a966a21b07744ce05063ae8c68f09156c47717fcff825875f82b4535f945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235649"
---
# <a name="autoradiobutton-control"></a>AUTOGRAMMBUTTON-Steuerelement

Definiert ein automatisches Optionsfeld-Steuerelement. Dieses Steuerelement führt automatisch den gegenseitigen Ausschluss mit den anderen **AUTOGRAMMBUTTON-Steuerelementen** in derselben Gruppe aus. Wenn die Schaltfläche ausgewählt wird, wird die Anwendung per **BN-KLICK \_ benachrichtigt.**

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der neben dem Optionsfeld angezeigt wird.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Stile für das automatische Optionsfeld, bei dem es sich um eine Kombination aus BUTTON-Klassenstilen und den folgenden Stilen sein kann: **WS \_ TABSTOP,** **WS \_ DISABLED** und **WS \_ GROUP**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Steuerung**](control-control.md)
</dt> <dt>

[Optionsfelder](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**Radiobutton**](radiobutton-control.md)
</dt> </dl>

 

 




