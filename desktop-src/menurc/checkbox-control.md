---
title: CHECKBOX-Steuerelement (Ressourcencompiler)
description: Definiert ein Kontrollkästchen-Steuerelement.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- CHECKBOX-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461330"
---
# <a name="checkbox-control"></a>CHECKBOX-Steuerelement

Definiert ein Kontrollkästchen-Steuerelement. Das Steuerelement ist ein kleines Rechteck (Kontrollkästchen), neben dem der angegebene Text angezeigt wird (in der Regel rechts). Wenn der Benutzer das Steuerelement auswählt, hebt das Steuerelement das Rechteck hervor und sendet eine Nachricht an das übergeordnete Fenster.

Die **CHECKBOX-Anweisung,** die nur in einer [**DIALOGEX-Anweisung**](dialogex-resource.md) verwendet werden kann, definiert den Text, bezeichner, Dimensionen und Attribute des Steuerelements.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der rechts vom Steuerelement angezeigt werden soll.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine Kombination aus den Stilen **BS \_ CHECKBOX** der Schaltflächenklasse und **WS \_ TABSTOP** und **WS \_ GROUP** sein.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Kontrollkästchen-Steuerelement mit der Bezeichnung Italic definiert:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Kontrollkästchen](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 