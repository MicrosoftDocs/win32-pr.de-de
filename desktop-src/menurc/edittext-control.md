---
title: EDITTEXT-Steuerelement
description: Definiert ein Bearbeitungs Steuerelement, das zur Edit-Klasse gehört.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- EDITTEXT-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725880"
---
# <a name="edittext-control"></a>EDITTEXT-Steuerelement

Definiert ein Bearbeitungs Steuerelement, das zur Edit-Klasse gehört. Es wird ein rechteckiger Bereich erstellt, in dem der Benutzer Text eingeben und bearbeiten kann. Das Steuerelement zeigt einen Cursor an, wenn der Benutzer auf die Maus klickt. Der Benutzer kann dann die Tastatur verwenden, um Text einzugeben oder den vorhandenen Text zu bearbeiten. Zum Bearbeiten von Schlüsseln gehören die Rücktaste und die Schlüssel zum Löschen. Der Benutzer kann auch mit der Maus Zeichen auswählen, die gelöscht werden sollen, oder den Ort auswählen, an dem neue Zeichen eingefügt werden sollen.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Bei diesem Wert kann es sich um eine Kombination der Stile der Bearbeitungs Klasse und der folgenden Stile handeln: **WS \_ Tabstopps**, **WS \_ Group**, **WS \_ VScroll**, **WS \_ HScroll** und **WS \_ deaktiviert**.

Wenn Sie keinen Stil angeben, ist der Standardstil `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **EDITTEXT** -Anweisung veranschaulicht:

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Steuerelemente bearbeiten](../controls/about-edit-controls.md)
</dt> </dl>

 

 