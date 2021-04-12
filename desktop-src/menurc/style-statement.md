---
title: Style-Anweisung
description: Definiert den Fenster Stil des Dialog Felds. Der Fenster Stil gibt an, ob das Feld ein Popup-oder ein untergeordnetes Fenster ist.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Stil Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390256"
---
# <a name="style-statement"></a>Style-Anweisung

Definiert den Fenster Stil des Dialog Felds. Der Fenster Stil gibt an, ob das Feld ein Popup-oder ein untergeordnetes Fenster ist.

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Der Fensterstil. Dieser Parameter kann ein ganzzahliger Wert oder eine Kombination aus Fenster Stil Werten (z. b. **WS \_ Caption** und **WS \_ sysmenu**) und Dialogfeld-Stil Werten (z. b. **DS \_ Center**) sein.

</dd> </dl>

Eine Liste der Fenster Stile finden Sie unter [Fenster Stile](/windows/desktop/winmsg/window-styles). Eine Liste der Dialogfeld Stile finden Sie unter [Dialogfeld Vorlagen Stile](../dlgbox/about-dialog-boxes.md). Wenn Sie die Werte für das Fenster oder den Dialogfeld Stil verwenden, müssen Sie Windows. h einschließen.

 

 