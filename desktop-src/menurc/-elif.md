---
title: " elif"
description: Die \ elif-Direktive markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine \ ifdef-, \ ifndef-oder \ if-Direktive definiert wird.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037097"
---
# <a name="elif"></a>\#elif

Die **\# elif** -Direktive markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine **\# ifdef**-, **\# ifndef**-oder **\# if** -Direktive definiert wird. Die-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Konstante Ausdruck überprüft wird. Wenn der Konstante Ausdruck ungleich NULL ist, weist **\# elif** den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive fortzusetzen und dann nach **\# EndIf** zur Anweisung zu springen. Wenn der Konstante Ausdruck 0 (null) ist, weist **\# elif** den Compiler an, zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive zu springen. Sie können eine beliebige Anzahl von **\# elif** -Direktiven in einem bedingten Block verwenden.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*Constant-Expression*
</dt> <dd>

Der zu überprüfende Ausdruck. Dieser Wert ist ein definierter Name, eine ganzzahlige Konstante oder ein Ausdruck, der aus Namen, Integern und arithmetischen und relationalen Operatoren besteht.

</dd> </dl>

## <a name="example"></a>Beispiel

In diesem Beispiel weist **\# elif** den Compiler an, die zweite [**Bitmap**](bitmap-resource.md) -Anweisung nur dann zu verarbeiten, wenn der Wert, der der namens Version zugewiesen ist, kleiner als 7 ist. Die **\# elif** -Direktive selbst wird nur verarbeitet, wenn die Version größer oder gleich 3 ist.

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

 

 




