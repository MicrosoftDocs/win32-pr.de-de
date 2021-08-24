---
title: " if"
description: Die \if-Direktive steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen konstanten Ausdrucks.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d898d0089ab6abeefb8c11e3a781446e498ed7c0f490545189987ec4857f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599711"
---
# <a name="if"></a>\#Wenn

Die **\# if-Direktive** steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen konstanten Ausdrucks. Wenn der konstante Ausdruck ungleich 0 (null) **\# ist,** , wenn den Compiler anweise, die Verarbeitung von Anweisungen bis zur nächsten **\# Endif-,** **\# else-** oder **\# elif-Direktive** fortzufahren, und dann mit der Anweisung nach der **\# endif-Direktive** springen. Wenn der konstante Ausdruck 0 (null) **\# ist,** wenn den Compiler anweise, mit der nächsten **\# endif-,** **\# else-** oder **\# elif-Direktive zu** springen.

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Der zu überprüfende Ausdruck. Dieser Wert ist ein definierter Name, eine ganzzahlige Konstante oder ein Ausdruck, der aus Namen, ganzen Zahlen und arithmetischen und relationalen Operatoren besteht.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel wird die [**BITMAP-Anweisung**](bitmap-resource.md) nur kompiliert, wenn der zugewiesene Wert Version kleiner als 3 ist:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




