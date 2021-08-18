---
title: COMBOBOX-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Kombinationsfeld-Steuerelement (ein Kombinationsfeld).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- COMBOBOX-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2ffaa64266d9b370cca5215725eb45d0f620054c66562e3f60492441e38890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972119"
---
# <a name="combobox-control"></a>COMBOBOX-Steuerelement

Definiert ein Kombinationsfeld-Steuerelement (ein Kombinationsfeld). Ein Kombinationsfeld besteht entweder aus einem statischen Textfeld oder einem Bearbeitungsfeld in Kombination mit einem Listenfeld. Das Listenfeld kann jederzeit angezeigt oder vom Benutzer heruntergefahren werden. Wenn das Kombinationsfeld ein statisches Textfeld enthält, zeigt das Textfeld immer die Auswahl (sofern verfügbar) im Listenfeldbereich des Kombinationsfelds an. Wenn ein Bearbeitungsfeld verwendet wird, kann der Benutzer die gewünschte Auswahl eingeben. Im Listenfeld wird das erste Element (sofern verfügbar) angezeigt, das mit dem im Bearbeitungsfeld eingegebenen Element entspricht. Der Benutzer kann dann das im Listenfeld hervorgehobene Element auswählen, um die Auswahl zu treffen. Darüber hinaus kann das Kombinationsfeld vom Besitzer gezeichnet werden und eine feste oder variable Höhe haben.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine Kombination aus den COMBOBOX-Klassenstilen und einem der folgenden Stile sein: **WS \_ TABSTOP,** **WS \_ GROUP,** **WS \_ VSCROLL** und **WS \_ DISABLED**.

Wenn Sie keinen Stil angeben, ist der Standardstil `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

Der *Height-Parameter* gilt für die Höhe eines Kombinationsfelds mit einer vollständig erweiterten Dropdownliste.

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Kombinationsfeld-Steuerelement mit einer vertikalen Bildlaufleiste definiert:

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kombinationsfelder](../controls/about-combo-boxes.md)
</dt> </dl>

 

 