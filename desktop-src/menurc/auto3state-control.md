---
title: AUTO3STATE-Steuerelement
description: Definiert ein automatisches Kontrollkästchen mit drei Zuständen.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- AUTO3STATE-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318d43f0b6d8a16d6e76ae3d12f934e41e265197690a955cfe148dd71176f440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735212"
---
# <a name="auto3state-control"></a>AUTO3STATE-Steuerelement

Definiert ein automatisches Kontrollkästchen mit drei Zuständen. Das Steuerelement ist ein offenes Feld mit dem angegebenen Text, der rechts neben dem Feld positioniert ist. Wenn diese Option aktiviert ist, wird das Kontrollkästchen automatisch zwischen drei Zuständen erweitert: aktiviert, deaktiviert und deaktiviert (grau). Das Steuerelement sendet immer dann eine Nachricht an sein übergeordnetes Element, wenn der Benutzer das Steuerelement ausgibt.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Stile für das Steuerelement, die eine Kombination aus dem **BS \_ AUTO3STATE-Stil** und den folgenden Stilen sein können: **WS \_ TABSTOP**, **WS \_ DISABLED** und **WS \_ GROUP**.

Wenn Sie keinen Stil angeben, lautet der Standardstil `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Kontrollkästchen](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Checkbox**](checkbox-control.md)
</dt> <dt>

[**Steuerung**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Fensterstile](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 