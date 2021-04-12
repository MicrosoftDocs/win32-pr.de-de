---
title: ComboBox-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Kombinations Feld-Steuerelement (ein Kombinations Feld).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menüs für ComboBox-Steuerelemente und andere Ressourcen
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390209"
---
# <a name="combobox-control"></a>ComboBox-Steuerelement

Definiert ein Kombinations Feld-Steuerelement (ein Kombinations Feld). Ein Kombinations Feld besteht aus einem statischen Textfeld oder einem Bearbeitungsfeld, das mit einem Listenfeld kombiniert ist. Das Listenfeld kann jederzeit angezeigt oder vom Benutzer abgerufen werden. Wenn das Kombinations Feld ein statisches Textfeld enthält, zeigt das Textfeld immer die Auswahl (sofern vorhanden) im Listenfeld Bereich des Kombinations Felds an. Wenn ein Bearbeitungsfeld verwendet wird, kann der Benutzer die gewünschte Auswahl eingeben. im Listenfeld wird das erste Element (sofern vorhanden) hervorgehoben, das dem entspricht, was der Benutzer im Bearbeitungsfeld eingegeben hat. Der Benutzer kann dann das im Listenfeld hervorgehobene Element auswählen, um die Auswahl abzuschließen. Außerdem kann das Kombinations Feld vom Besitzer gezeichnet werden und eine Höhe mit fester oder variabler Höhe aufweisen.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine Kombination der ComboBox-Klassen Stile und eines der folgenden Stile handeln: " **WS \_ Tabstopps**", " **WS \_ Group**", " **WS \_ VScroll**" und " **WS \_ deaktiviert**".

Wenn Sie keinen Stil angeben, ist der Standardstil `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

Der *height* -Parameter gilt für die Höhe eines Kombinations Felds, in dem eine Dropdown Liste vollständig erweitert ist.

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Kombinations Feld-Steuerelement mit einer vertikalen Scrollleiste definiert:

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kombinations Felder](../controls/about-combo-boxes.md)
</dt> </dl>

 

 