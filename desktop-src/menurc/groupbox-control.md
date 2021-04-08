---
title: GroupBox-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Gruppenfeld-Steuerelement. Das-Steuerelement ist ein Rechteck, in dem andere Steuerelemente gruppiert werden. Die Steuerelemente werden gruppiert, indem Sie einen Rahmen herum zeichnen und den angegebenen Text in der oberen linken Ecke anzeigen.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- GroupBox-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104038301"
---
# <a name="groupbox-control"></a>GroupBox-Steuerelement

Definiert ein Gruppenfeld-Steuerelement. Das-Steuerelement ist ein Rechteck, in dem andere Steuerelemente gruppiert werden. Die Steuerelemente werden gruppiert, indem Sie einen Rahmen herum zeichnen und den angegebenen Text in der oberen linken Ecke anzeigen.

Die **GroupBox** -Anweisung, die Sie nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwenden können, definiert den Text, den Bezeichner, die Dimensionen und die Attribute eines Steuerelement Fensters.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine Kombination aus der Schaltfläche "Class Style" der Schaltfläche " **\_ GroupBox** **" und den Stilen " \_** **WS \_ Tabstopps** "

Wenn Sie keinen Stil angeben, ist der Standardstil " **SB \_ GroupBox**".

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="remarks"></a>Bemerkungen

Wenn der Stil **WS \_ Tabstopps** enthält oder der Text eine Zugriffstaste angibt, verschiebt die Tab-Taste oder das Drücken der Tastenkombination den Fokus auf das erste Steuerelement in der Gruppe.

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Gruppenfeld-Steuerelement mit der Bezeichnung "Options" definiert:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Gruppenfelder](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




