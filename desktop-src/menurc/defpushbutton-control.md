---
title: DEFPUSHBUTTON-Steuerelement
description: Definiert ein Standardmäßiges Push-Button-Steuerelement.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- DEFPUSHBUTTON-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338233"
---
# <a name="defpushbutton-control"></a>DEFPUSHBUTTON-Steuerelement

Definiert ein Standardmäßiges Push-Button-Steuerelement. Das-Steuerelement ist ein kleines Rechteck mit einem fetten Umriss, der die Standardantwort für den Benutzer darstellt. Der angegebene Text wird in der Schaltfläche angezeigt. Das-Steuerelement hebt die Schaltfläche auf die übliche Weise hervor, wenn der Benutzer mit der Maus darauf klickt und eine Meldung an das übergeordnete Fenster sendet.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der im rechteckigen Bereich des-Steuer Elements zentriert werden soll.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine Kombination der folgenden Stile handeln: " **SB \_ DEFPUSHBUTTON**", " **WS \_ Tabstopps**", " **WS \_ Group**" und " **WS \_**"

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Standardmäßiges Push-Button-Steuerelement mit der Bezeichnung Abbrechen definiert:

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Pushschaltflächen](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**PUSHBUTTON**](pushbutton-control.md)
</dt> <dt>

[**RadioButton**](radiobutton-control.md)
</dt> </dl>

 

 




