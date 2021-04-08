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
# <a name="elif"></a><span data-ttu-id="97995-103">\#elif</span><span class="sxs-lookup"><span data-stu-id="97995-103">\#elif</span></span>

<span data-ttu-id="97995-104">Die **\# elif** -Direktive markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine **\# ifdef**-, **\# ifndef**-oder **\# if** -Direktive definiert wird.</span><span class="sxs-lookup"><span data-stu-id="97995-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="97995-105">Die-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Konstante Ausdruck überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="97995-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="97995-106">Wenn der Konstante Ausdruck ungleich NULL ist, weist **\# elif** den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive fortzusetzen und dann nach **\# EndIf** zur Anweisung zu springen.</span><span class="sxs-lookup"><span data-stu-id="97995-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="97995-107">Wenn der Konstante Ausdruck 0 (null) ist, weist **\# elif** den Compiler an, zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive zu springen.</span><span class="sxs-lookup"><span data-stu-id="97995-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="97995-108">Sie können eine beliebige Anzahl von **\# elif** -Direktiven in einem bedingten Block verwenden.</span><span class="sxs-lookup"><span data-stu-id="97995-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="97995-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*Constant-Expression*</span><span class="sxs-lookup"><span data-stu-id="97995-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="97995-110">Der zu überprüfende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="97995-110">Expression to be checked.</span></span> <span data-ttu-id="97995-111">Dieser Wert ist ein definierter Name, eine ganzzahlige Konstante oder ein Ausdruck, der aus Namen, Integern und arithmetischen und relationalen Operatoren besteht.</span><span class="sxs-lookup"><span data-stu-id="97995-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="97995-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97995-112">Example</span></span>

<span data-ttu-id="97995-113">In diesem Beispiel weist **\# elif** den Compiler an, die zweite [**Bitmap**](bitmap-resource.md) -Anweisung nur dann zu verarbeiten, wenn der Wert, der der namens Version zugewiesen ist, kleiner als 7 ist.</span><span class="sxs-lookup"><span data-stu-id="97995-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="97995-114">Die **\# elif** -Direktive selbst wird nur verarbeitet, wenn die Version größer oder gleich 3 ist.</span><span class="sxs-lookup"><span data-stu-id="97995-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="97995-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97995-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97995-116">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="97995-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




