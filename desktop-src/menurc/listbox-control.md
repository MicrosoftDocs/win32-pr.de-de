---
title: LISTBOX-Steuerelement (Menüs und andere Ressourcen)
description: Definiert häufig verwendete Steuerelemente für ein Dialogfeld oder Fenster. Das Steuerelement ist ein Rechteck, das eine Liste von Zeichenfolgen (z. B. Dateinamen) enthält, aus denen der Benutzer auswählen kann.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- 'LISTBOX-Steuerelement: Menüs und andere Ressourcen'
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676ea07f7d66a0d84997f0b2b22b9973c326db0fb603caedcc631caeffffaf98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226348"
---
# <a name="listbox-control"></a>LISTBOX-Steuerelement

Definiert häufig verwendete Steuerelemente für ein Dialogfeld oder Fenster. Das Steuerelement ist ein Rechteck, das eine Liste von Zeichenfolgen (z. B. Dateinamen) enthält, aus denen der Benutzer auswählen kann.

Die **LISTBOX-Anweisung,** die nur in einer [**DIALOGEX-**](dialogex-resource.md) oder **WINDOW-Anweisung** verwendet werden kann, definiert den Bezeichner, die Dimensionen und die Attribute eines Steuerelementfensters.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine Kombination aus den Listenfeldklassenstilen und einem der folgenden Stile sein: **WS \_ BORDER** und **WS \_ VSCROLL.**

Wenn Sie keinen Stil angeben, lautet der Standardstil `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Listenfeld-Steuerelement definiert, dessen Bezeichner 101 ist:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Combobox**](combobox-control.md)
</dt> <dt>

[Listenfelder](../controls/about-list-boxes.md)
</dt> </dl>

 

 