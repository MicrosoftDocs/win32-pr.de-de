---
title: Rtext-Steuerelement
description: Definiert ein rechts Bündiges Text Steuerelement.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Rtext-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473093"
---
# <a name="rtext-control"></a>Rtext-Steuerelement

Definiert ein rechts Bündiges Text Steuerelement. Das-Steuerelement ist ein einfaches Rechteck, das den angegebenen Text rechtsbündig im Rechteck anzeigt. Der Text wird formatiert, bevor er angezeigt wird. Wörter, die über das Ende einer Linie hinaus erweitert werden, werden automatisch an den Anfang der nächsten Zeile umschließt. Wörter, die länger als die Breite des Steuer Elements sind, werden abgeschnitten.

Die **rtext** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Stile für das Text Steuerelement, bei denen es sich um eine beliebige Kombination der folgenden Typen handeln kann: **WS \_ Tabstopps** und **WS- \_ Gruppe**.

Wenn Sie keinen Stil angeben, ist der Standardstil `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **rtext** -Anweisung veranschaulicht:

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Steuerelemente bearbeiten](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 