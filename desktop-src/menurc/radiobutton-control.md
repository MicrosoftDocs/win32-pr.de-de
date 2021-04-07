---
title: RadioButton-Steuerelement
description: Definiert ein Optionsfeld-Steuerelement.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- RadioButton-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038989"
---
# <a name="radiobutton-control"></a>RadioButton-Steuerelement

Definiert ein Optionsfeld-Steuerelement. Das-Steuerelement ist ein kleiner Kreis, in dem der angegebene Text daneben in der Regel rechts angezeigt wird. Das-Steuerelement hebt den Kreis hervor und sendet eine Meldung an das übergeordnete Fenster, wenn der Benutzer die Schaltfläche auswählt. Das-Steuerelement entfernt die Hervorhebung und sendet eine Meldung, wenn die Schaltfläche das nächste Mal ausgewählt wird.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Stile für das Optionsfeld, bei dem es sich um eine Kombination aus Schaltflächen Klassen Formaten und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ Deaktivierte** und **WS- \_ Gruppe**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **RadioButton** -Anweisung veranschaulicht:

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Options Felder](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 