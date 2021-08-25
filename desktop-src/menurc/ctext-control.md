---
title: CTEXT-Steuerelement
description: Definiert ein zentriertes Textsteuerfeld.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- CTEXT-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b220448fcaa6cbbbb6b01c605a9b5fd6e03f8dc6a60a0e409f6f275d9b74b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826000"
---
# <a name="ctext-control"></a>CTEXT-Steuerelement

Definiert ein zentriertes Textsteuerfeld. Das -Steuerelement ist ein einfaches Rechteck, das den angegebenen Text im Rechteck zentriert darstellt. Der Text wird formatiert, bevor er angezeigt wird. Wörter, die sich über das Ende einer Zeile erstrecken würden, werden automatisch bis zum Anfang der nächsten Zeile umschlossen. Wörter, die länger als die Breite des Steuerelements sind, werden abgeschnitten.

Die [**LTEXT-Anweisung,**](ltext-control.md) die nur in einer rep-Anweisung verwendet werden kann, definiert den Text, bezeichner, Dimensionen und Attribute des Steuerelements.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der im rechteckigen Bereich des Steuerelements zentriert werden soll.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine beliebige Kombination der folgenden Stile sein: **SS \_ CENTER,** **WS \_ TABSTOP** und **WS \_ GROUP**.

Wenn Sie keinen Stil angeben, ist der Standardstil `SS_CENTER | WS_GROUP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein zentriertes Text-Steuerelement mit der Bezeichnung Dateiname definiert:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Steuerung**](control-control.md)
</dt> <dt>

[Bearbeiten von Steuerelementen](../controls/about-edit-controls.md)
</dt> <dt>

[**Ltext**](ltext-control.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 