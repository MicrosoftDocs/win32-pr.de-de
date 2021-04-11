---
title: PUSHBUTTON-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Push-Button-Steuerelement. Das-Steuerelement ist ein Rechteck mit runden Kurven, das den angegebenen Text enthält. Der Text wird im-Steuerelement zentriert. Das-Steuerelement sendet eine Meldung an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menüs für PUSHBUTTON-Steuerelemente und andere Ressourcen
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315129"
---
# <a name="pushbutton-control"></a>PUSHBUTTON-Steuerelement

Definiert ein Push-Button-Steuerelement. Das-Steuerelement ist ein Rechteck mit runden Kurven, das den angegebenen Text enthält. Der Text wird im-Steuerelement zentriert. Das-Steuerelement sendet eine Meldung an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Stile für die PUSHBUTTON-Datei, bei der es sich um eine Kombination aus der Art der Karten **Schaltfläche \_** und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ deaktiviert** und **WS- \_ Gruppe**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **PUSHBUTTON** -Anweisung veranschaulicht:

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Pushschaltflächen](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 