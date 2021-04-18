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
# <a name="if"></a><span data-ttu-id="37644-103">\#sei</span><span class="sxs-lookup"><span data-stu-id="37644-103">\#if</span></span>

<span data-ttu-id="37644-104">Die **\# if** -Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Konstante Ausdruck überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="37644-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="37644-105">Wenn der Konstante Ausdruck ungleich NULL ist, weist den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive fortzusetzen, und dann mit der Anweisung nach der **\# EndIf** -Direktive zu springen. **\#**</span><span class="sxs-lookup"><span data-stu-id="37644-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="37644-106">Wenn der Konstante Ausdruck 0 (null) ist, weist den Compiler an, die nächste **\# EndIf**-, **\# else**-oder **\# elif** -Direktive zu überspringen. **\#**</span><span class="sxs-lookup"><span data-stu-id="37644-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="37644-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*Constant-Expression*</span><span class="sxs-lookup"><span data-stu-id="37644-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="37644-108">Der zu überprüfende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="37644-108">Expression to be checked.</span></span> <span data-ttu-id="37644-109">Dieser Wert ist ein definierter Name, eine ganzzahlige Konstante oder ein Ausdruck, der aus Namen, Integern und arithmetischen und relationalen Operatoren besteht.</span><span class="sxs-lookup"><span data-stu-id="37644-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="37644-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="37644-110">Example</span></span>

<span data-ttu-id="37644-111">In diesem Beispiel wird die [**Bitmap**](bitmap-resource.md) -Anweisung nur kompiliert, wenn der zugewiesene Wert Version kleiner als 3 ist:</span><span class="sxs-lookup"><span data-stu-id="37644-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="37644-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37644-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37644-113">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="37644-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




