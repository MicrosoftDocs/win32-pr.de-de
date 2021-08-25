---
title: " elif"
description: Die \elif-Direktive markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine \ifdef-, \ifndef- oder \if-Anweisung definiert wird.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e131d40648bcda75025087717798ceb2ad1262d680877512dbb85a451fc86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720900"
---
# <a name="elif"></a>\#Elif

Die **\# elif-Direktive** markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine **\# ifdef-,** **\# ifndef-** oder **\# if-Anweisung** definiert wird. Die -Direktive steuert die bedingte Kompilierung der Ressourcendatei durch Überprüfen des angegebenen konstanten Ausdrucks. Wenn der konstante Ausdruck ungleich 0 (null) ist, weist **\# elif** den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# endif-,** **\# andernfalls**- oder **\# elif-Direktive** fortzusetzen und dann nach **\# endif** zur -Anweisung zu springen. Wenn der konstante Ausdruck 0 (null) ist, weist **\# elif** den Compiler an, zur nächsten **\# endif-,** **\# else-** oder **\# elif-Direktive** zu springen. Sie können eine beliebige Anzahl von **\# Elif-Direktiven** in einem bedingten Block verwenden.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Der zu überprüfende Ausdruck. Dieser Wert ist ein definierter Name, eine ganzzahlige Konstante oder ein Ausdruck, der aus Namen, ganzen Zahlen und arithmetischen und relationalen Operatoren besteht.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel weist **\# elif** den Compiler an, die zweite [**BITMAP-Anweisung**](bitmap-resource.md) nur zu verarbeiten, wenn der wert, der dem Namen Version zugewiesen ist, kleiner als 7 ist. Die **\# elif-Direktive** selbst wird nur verarbeitet, wenn Version größer oder gleich 3 ist.

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven](preprocessor-directives.md)
</dt> </dl>

 

 




