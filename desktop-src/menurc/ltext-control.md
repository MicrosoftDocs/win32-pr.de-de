---
title: LTEXT-Steuerelement
description: Definiert ein Links Bündiges Text Steuerelement.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- LTEXT-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340702"
---
# <a name="ltext-control"></a>LTEXT-Steuerelement

Definiert ein Links Bündiges Text Steuerelement. Das-Steuerelement ist ein einfaches Rechteck, das den angegebenen Text linksbündig im Rechteck anzeigt. Der Text wird formatiert, bevor er angezeigt wird. Wörter, die über das Ende einer Linie hinaus erweitert werden, werden automatisch an den Anfang der nächsten Zeile umschließt. Wörter, die länger als die Breite des Steuer Elements sind, werden abgeschnitten.

Die **LTEXT** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine beliebige Kombination aus dem **\_ RadioButton** -Stil von "SB" und den folgenden Stilen handeln: **SS \_ left**, **WS \_ Tabstopps** und **WS \_ Group**.

Wenn Sie keinen Stil angeben, ist der Standardstil `SS_LEFT | WS_GROUP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Links Bündiges Text Steuerelement mit der Bezeichnung "filename" definiert:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Steuerelemente bearbeiten](../controls/about-edit-controls.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 