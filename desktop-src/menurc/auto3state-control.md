---
title: AUTO3STATE-Steuerelement
description: Definiert ein automatisches Kontrollkästchen mit drei Zuständen.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- AUTO3STATE-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101558"
---
# <a name="auto3state-control"></a>AUTO3STATE-Steuerelement

Definiert ein automatisches Kontrollkästchen mit drei Zuständen. Das-Steuerelement ist ein geöffnetes Feld mit dem angegebenen Text, der rechts neben dem Feld positioniert ist. Wenn diese Option ausgewählt ist, wechselt das Feld automatisch zwischen drei Zuständen: aktiviert, deaktiviert und deaktiviert (grau). Das-Steuerelement sendet eine Meldung an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Stile für das-Steuerelement, bei dem es sich um eine Kombination aus dem **\_ AUTO3STATE** -Format und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ Deaktivierte** und **WS- \_ Gruppe**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Kontrollkästchen](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Markieren**](checkbox-control.md)
</dt> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Fensterstile](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 