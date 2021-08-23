---
title: ICON-Steuerelement
description: Definiert ein Symbolsteuerzeichen. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- ICON-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fc5191457996aabe4a70fefcf64235b3a9573cf12733f9ca7bff2ece6356e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034288"
---
# <a name="icon-control"></a>ICON-Steuerelement

Definiert ein Symbolsteuerzeichen. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird.

Die  ICON-Steuerelement-Anweisung, die Sie nur in einer [**DIALOGEX-Anweisung**](dialogex-resource.md) verwenden können, definiert den Symbolressourcenbezeichner, den Symbolsteuersteuerzeichner, die Position und die Attribute eines Steuerelements.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Der Name eines Symbols (kein Dateiname), das an anderer Stelle in der Ressourcendatei definiert ist.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Breite*
</dt> <dd>

Dieser Wert wird ignoriert und sollte auf 0 (null) festgelegt werden.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Höhe*
</dt> <dd>

Dieser Wert wird ignoriert und sollte auf 0 (null) festgelegt werden.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstil. Dieser Parameter ist optional. Der einzige Wert, der angegeben werden kann, ist das **SS \_ ICON-Format.** Dies ist der Standardstil, unabhängig davon, ob dieser Parameter angegeben wird oder nicht.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

In diesem Beispiel wird ein Symbolsteuerzeichen definiert, dessen Symbolbezeichner 901 ist und dessen Name myicon ist:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Symbol**](icon-resource.md)
</dt> </dl>

 

 




