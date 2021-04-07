---
title: AUTOCHECKBOX-Steuerelement
description: Definiert ein automatisches Kontrollkästchen-Steuerelement.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menüs für AUTOCHECKBOX-Steuerelemente und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725560"
---
# <a name="autocheckbox-control"></a>AUTOCHECKBOX-Steuerelement

Definiert ein automatisches Kontrollkästchen-Steuerelement. Das-Steuerelement ist ein kleines Rechteck (Kontrollkästchen), das neben dem angegebenen Text angezeigt wird (in der Regel rechts). Wenn der Benutzer das Steuerelement auswählt, hebt das-Steuerelement das Rechteck hervor und sendet eine Meldung an das übergeordnete Fenster.

Die **AUTOCHECKBOX** -Anweisung kann nur im Text einer [**Dialog**](dialog-resource.md) -oder [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden.

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Stile des Steuer Elements. Bei diesem Wert kann es sich um eine Kombination aus der Schaltfläche "Button" der Schaltfläche " **\_ AUTOCHECKBOX** " und " **WS \_ Tabstopps** " und " **WS \_**

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTOCHECKBOX | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Schaltflächenstile](../controls/button-styles.md)
</dt> <dt>

[**Markieren**](checkbox-control.md)
</dt> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 