---
title: Symbol Steuerelement
description: Definiert ein Symbol Steuerelement. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Symbol Steuerungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471917"
---
# <a name="icon-control"></a>Symbol Steuerelement

Definiert ein Symbol Steuerelement. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird.

Die **Symbol** Steuerungs Anweisung, die Sie nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwenden können, definiert den Symbol Ressourcen Bezeichner, den Symbol Steuerelement Bezeichner, die Position und die Attribute eines Steuer Elements.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Der Name eines Symbols (kein Dateiname), der an anderer Stelle in der Ressourcen Datei definiert ist.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Breite*
</dt> <dd>

Dieser Wert wird ignoriert und sollte auf 0 (null) festgelegt werden.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Flugh*
</dt> <dd>

Dieser Wert wird ignoriert und sollte auf 0 (null) festgelegt werden.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stil. Dieser Parameter ist optional. Der einzige Wert, der angegeben werden kann, ist der **SS- \_** Symbolstil. Dies ist der Standardstil, unabhängig davon, ob dieser Parameter angegeben wird.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Symbol Steuerelement definiert, dessen Symbol Bezeichner 901 und dessen Name "myIcon" lautet:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Angezeigt**](icon-resource.md)
</dt> </dl>

 

 




