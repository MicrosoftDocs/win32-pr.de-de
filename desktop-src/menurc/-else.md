---
title: " else"
description: Die Direktive "\ Else" markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine \ ifdef-, \ ifndef-oder \ if-Direktive definiert wird. Die \ Else-Direktive muss die letzte Direktive vor der \ endif-Direktive sein.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710913"
---
# <a name="else"></a><span data-ttu-id="37459-104">\#else</span><span class="sxs-lookup"><span data-stu-id="37459-104">\#else</span></span>

<span data-ttu-id="37459-105">Die **\# else** -Direktive markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung, der durch eine **\# ifdef**-, **\# ifndef**-oder **\# if** -Direktive definiert wird.</span><span class="sxs-lookup"><span data-stu-id="37459-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="37459-106">Die **\# else** -Direktive muss die letzte Direktive vor der **\# EndIf** -Direktive sein.</span><span class="sxs-lookup"><span data-stu-id="37459-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="37459-107">Diese Direktive hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="37459-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="37459-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="37459-108">Example</span></span>

<span data-ttu-id="37459-109">In diesem Beispiel wird die zweite [**Bitmap**](bitmap-resource.md) -Anweisung nur dann kompiliert, wenn Debug nicht definiert ist:</span><span class="sxs-lookup"><span data-stu-id="37459-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="37459-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37459-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37459-111">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="37459-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




