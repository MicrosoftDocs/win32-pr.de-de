---
title: ScrollBar-Steuerelement
description: Definiert ein ScrollBar-Steuerelement.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- ScrollBar-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101635"
---
# <a name="scrollbar-control"></a>ScrollBar-Steuerelement

Definiert ein ScrollBar-Steuerelement. Das-Steuerelement ist ein Rechteck, das ein Bild Lauf Feld mit Richtungs Pfeilen an beiden Enden enthält. Das Bild Lauf leisten-Steuerelement sendet eine Benachrichtigungs Meldung an das übergeordnete Element, wenn der Benutzer im Steuerelement auf die Maus klickt. Das übergeordnete Element ist für das Aktualisieren der scrollfeldposition verantwortlich. Bild Lauf leisten-Steuerelemente können an beliebiger Stelle in einem Fenster positioniert und bei Bedarf verwendet werden, um scrolleingaben bereitzustellen.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

NULL oder eine Kombination der folgenden Stile: **WS \_ Tabstopps**, **WS \_ Group** und **WS \_ deaktiviert**.

Zusätzlich zu diesen Stilen kann der *Style* -Parameter eine Kombination (oder keine) der ScrollBar-Klassen Stile enthalten.

Wenn Sie keinen Stil angeben, ist der Standardstil **SSB \_ Horz**.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md). Beachten Sie, dass Sie für dieses Steuerelement keinen Text angeben können.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **ScrollBar** -Anweisung veranschaulicht:

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Scrollleisten](../controls/about-scroll-bars.md)
</dt> </dl>

 

 