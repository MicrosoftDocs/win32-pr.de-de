---
title: " ifndef"
description: Die \ ifndef-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341237"
---
# <a name="ifndef"></a><span data-ttu-id="dc264-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="dc264-103">\#ifndef</span></span>

<span data-ttu-id="dc264-104">Die **\# ifndef** -Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="dc264-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="dc264-105">Wenn der Name nicht definiert wurde oder seine Definition mithilfe der **\# undef** -Direktive entfernt wurde, weist **\# ifndef** den Compiler an, die Verarbeitung von Anweisungen bis zur nächsten **\# EndIf**-, **\# else**-oder **\# elif** -Direktive fortzusetzen und die Anweisung nach der **\# EndIf** -Direktive zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="dc264-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="dc264-106">Wenn der Name definiert ist, leitet **\# ifndef** den Compiler an, die nächste **\# EndIf**-, **\# else**-oder **\# elif** -Direktive zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="dc264-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="dc264-107"><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="dc264-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="dc264-108">Der Name, der von der Direktive geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc264-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="dc264-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dc264-109">Example</span></span>

<span data-ttu-id="dc264-110">In diesem Beispiel wird die [**Bitmap**](bitmap-resource.md) -Anweisung nur kompiliert, wenn die Optimierung nicht definiert ist:</span><span class="sxs-lookup"><span data-stu-id="dc264-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="dc264-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc264-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc264-112">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="dc264-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




