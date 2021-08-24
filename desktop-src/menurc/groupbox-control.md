---
title: GROUPBOX-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Gruppenfeld-Steuerelement. Das Steuerelement ist ein Rechteck, das andere Steuerelemente gruppiert. Die Steuerelemente werden gruppiert, indem ein Rahmen um sie gezeichnet und der angegebene Text in der oberen linken Ecke angezeigt wird.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- 'GROUPBOX-Steuerelement: Menüs und andere Ressourcen'
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05fb8e795cfe483d16406f07fffd2a26df14cebc3c38a07fbef7f2cb78cc245a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602080"
---
# <a name="groupbox-control"></a>GROUPBOX-Steuerelement

Definiert ein Gruppenfeld-Steuerelement. Das Steuerelement ist ein Rechteck, das andere Steuerelemente gruppiert. Die Steuerelemente werden gruppiert, indem ein Rahmen um sie gezeichnet und der angegebene Text in der oberen linken Ecke angezeigt wird.

Die **GROUPBOX-Anweisung,** die Sie nur in einer [**DIALOGEX-Anweisung**](dialogex-resource.md) verwenden können, definiert den Text, bezeichner, Dimensionen und Attribute eines Steuerelementfensters.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine Kombination aus dem **BS \_ GROUPBOX-Stil** der Schaltflächenklasse und den **Stilen WS \_ TABSTOP** und **WS \_ DISABLED** sein.

Wenn Sie keinen Stil angeben, lautet der Standardstil **BS \_ GROUPBOX**.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

## <a name="remarks"></a>Hinweise

Wenn der Stil **WS \_ TABSTOP** enthält oder der Text eine Zugriffstaste angibt, verschiebt das Drücken oder Drücken der Tastenkombination den Fokus auf das erste Steuerelement innerhalb der Gruppe.

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Gruppenfeld-Steuerelement mit der Bezeichnung Optionen definiert:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Gruppenfelder](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




