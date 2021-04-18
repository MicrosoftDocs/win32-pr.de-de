---
title: CheckBox-Steuerelement (Ressourcen Compiler)
description: Definiert ein Kontrollkästchen-Steuerelement.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- CheckBox-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337648"
---
# <a name="checkbox-control"></a>CheckBox-Steuerelement

Definiert ein Kontrollkästchen-Steuerelement. Das-Steuerelement ist ein kleines Rechteck (Kontrollkästchen), das neben dem angegebenen Text angezeigt wird (in der Regel rechts). Wenn der Benutzer das Steuerelement auswählt, hebt das-Steuerelement das Rechteck hervor und sendet eine Meldung an das übergeordnete Fenster.

Die **CheckBox** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der auf der rechten Seite des-Steuer Elements angezeigt werden soll.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine Kombination aus **dem \_ Kontrollkästchen** "Schaltfläche für Schaltflächen Klassen" und " **WS \_ Tabstopps** " und " **WS \_** "

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Kontrollkästchen-Steuerelement mit der Bezeichnung "Kursiv" definiert:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Siehe auch

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

 

 