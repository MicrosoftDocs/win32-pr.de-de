---
title: LTEXT-Steuerelement
description: Definiert ein linksbündig ausgerichtetes Textsteuerelement.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menüs und andere Ressourcen des LTEXT-Steuerelements
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdaafe752d547466267e8494743e8f0c99ccef0d0fb05b77db5dab2fa358f158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870274"
---
# <a name="ltext-control"></a>LTEXT-Steuerelement

Definiert ein linksbündig ausgerichtetes Textsteuerelement. Das Steuerelement ist ein einfaches Rechteck, das den angegebenen Text linksbündig im Rechteck anzeigt. Der Text wird formatiert, bevor er angezeigt wird. Wörter, die sich über das Ende einer Zeile erstrecken würden, werden automatisch bis zum Anfang der nächsten Zeile umschlossen. Wörter, die länger als die Breite des Steuerelements sind, werden abgeschnitten.

Die **LTEXT-Anweisung,** die nur in einer [**DIALOGEX-Anweisung**](dialogex-resource.md) verwendet werden kann, definiert den Text, bezeichner, Dimensionen und Attribute des Steuerelements.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine beliebige Kombination des **BS \_ RADIOBUTTON-Stils** und der folgenden Stile sein: **SS \_ LEFT,** **WS \_ TABSTOP** und **WS \_ GROUP.**

Wenn Sie keinen Stil angeben, lautet der Standardstil `SS_LEFT | WS_GROUP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein linksbündig ausgerichtetes Textsteuerelement mit der Bezeichnung Dateiname definiert:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Steuerung**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Bearbeiten von Steuerelementen](../controls/about-edit-controls.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 