---
title: " if"
description: Die \ if-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Konstante Ausdruck überprüft wird.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338587"
---
# <a name="if"></a>\#sei

Die **\# if** -Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Konstante Ausdruck überprüft wird. Wenn der Konstante Ausdruck ungleich NULL ist, weist den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive fortzusetzen, und dann mit der Anweisung nach der **\# EndIf** -Direktive zu springen. **\#** Wenn der Konstante Ausdruck 0 (null) ist, weist den Compiler an, die nächste **\# EndIf**-, **\# else**-oder **\# elif** -Direktive zu überspringen. **\#**

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*Constant-Expression*
</dt> <dd>

Der zu überprüfende Ausdruck. Dieser Wert ist ein definierter Name, eine ganzzahlige Konstante oder ein Ausdruck, der aus Namen, Integern und arithmetischen und relationalen Operatoren besteht.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel wird die [**Bitmap**](bitmap-resource.md) -Anweisung nur kompiliert, wenn der zugewiesene Wert Version kleiner als 3 ist:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




