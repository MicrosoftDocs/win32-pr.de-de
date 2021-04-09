---
title: ListBox-Steuerelement (Menüs und andere Ressourcen)
description: Definiert häufig verwendete Steuerelemente für ein Dialogfeld oder Fenster. Das-Steuerelement ist ein Rechteck, das eine Liste von Zeichen folgen enthält (z. b. Dateinamen), aus denen der Benutzer auswählen kann.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- ListBox-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101607"
---
# <a name="listbox-control"></a>ListBox-Steuerelement

Definiert häufig verwendete Steuerelemente für ein Dialogfeld oder Fenster. Das-Steuerelement ist ein Rechteck, das eine Liste von Zeichen folgen enthält (z. b. Dateinamen), aus denen der Benutzer auswählen kann.

Die **ListBox** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -oder **Window** -Anweisung verwendet werden kann, definiert den Bezeichner, die Dimensionen und die Attribute eines Steuerelement Fensters.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine Kombination der Listenfeld Klassen Stile und eines der folgenden Stile handeln: **WS \_ Border** und **WS \_ VScroll**.

Wenn Sie keinen Stil angeben, ist der Standardstil `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Listenfeld-Steuerelement definiert, dessen Bezeichner 101 ist:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ComboBox**](combobox-control.md)
</dt> <dt>

[Listenfelder](../controls/about-list-boxes.md)
</dt> </dl>

 

 