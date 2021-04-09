---
title: CTEXT-Steuerelement
description: Definiert ein zentriertes Text Steuerelement.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- CTEXT-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101554"
---
# <a name="ctext-control"></a>CTEXT-Steuerelement

Definiert ein zentriertes Text Steuerelement. Das-Steuerelement ist ein einfaches Rechteck, das den angegebenen Text anzeigt, der im Rechteck zentriert ist. Der Text wird formatiert, bevor er angezeigt wird. Wörter, die über das Ende einer Linie hinaus erweitert werden, werden automatisch an den Anfang der nächsten Zeile umschließt. Wörter, die länger als die Breite des Steuer Elements sind, werden abgeschnitten.

Die [**LTEXT**](ltext-control.md) -Anweisung, die nur in einer Rep-Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der im rechteckigen Bereich des-Steuer Elements zentriert werden soll.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine beliebige Kombination der folgenden Stile handeln: **SS \_ Center**, **WS \_ Tabstopps** und **WS \_ Group**.

Wenn Sie keinen Stil angeben, ist der Standardstil `SS_CENTER | WS_GROUP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein zentriert-Text-Steuerelement mit der Bezeichnung "filename" definiert:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[Steuerelemente bearbeiten](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 