---
title: SCROLLBAR-Steuerelement
description: Definiert ein Bildlaufleisten-Steuerelement.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- 'SCROLLBAR-Steuerelement: Menüs und andere Ressourcen'
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b03865f66a06198cc1b1b78f8bb0b0213d998b7e5407506e4b8ed64ed9efaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733438"
---
# <a name="scrollbar-control"></a>SCROLLBAR-Steuerelement

Definiert ein Bildlaufleisten-Steuerelement. Das Steuerelement ist ein Rechteck, das ein Bildlauffeld enthält und an beiden Enden Richtungspfeile hat. Das Bildlaufleisten-Steuerelement sendet immer dann eine Benachrichtigung an das übergeordnete Element, wenn der Benutzer im Steuerelement mit der Maus klickt. Das übergeordnete Element ist für die Aktualisierung der Scrollfeldposition verantwortlich. Scrollleisten-Steuerelemente können an einer beliebigen Stelle in einem Fenster positioniert und bei Bedarf verwendet werden, um Bildlaufeingaben bereitzustellen.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

0 (null) oder eine Kombination der folgenden Stile: **WS \_ TABSTOP**, **WS \_ GROUP** und **WS \_ DISABLED**.

Zusätzlich zu diesen Stilen kann der *style-Parameter* eine Kombination (oder keinen) der SCROLLBAR-Klassenstile enthalten.

Wenn Sie keinen Stil angeben, lautet der Standardstil **SBS \_ HORZ**.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md) Beachten Sie, dass Sie keinen Text für dieses Steuerelement angeben können.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **SCROLLBAR-Anweisung** veranschaulicht:

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Scrollleisten](../controls/about-scroll-bars.md)
</dt> </dl>

 

 