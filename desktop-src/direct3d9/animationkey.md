---
description: Definiert einen Satz von Animations Schlüsseln. Ein Matrix Schlüssel ist nützlich für Sätze von Animationsdaten, die als Transformations Matrizen dargestellt werden müssen.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: Animationkey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345452"
---
# <a name="animationkey"></a><span data-ttu-id="cc7a6-104">Animationkey</span><span class="sxs-lookup"><span data-stu-id="cc7a6-104">AnimationKey</span></span>

<span data-ttu-id="cc7a6-105">Definiert einen Satz von Animations Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-105">Defines a set of animation keys.</span></span> <span data-ttu-id="cc7a6-106">Ein Matrix Schlüssel ist nützlich für Sätze von Animationsdaten, die als Transformations Matrizen dargestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-106">A matrix key is useful for sets of animation data that need to be represented as transformation matrices.</span></span>

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

<span data-ttu-id="cc7a6-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="cc7a6-107">Where:</span></span>

-   <span data-ttu-id="cc7a6-108">KeyType: gibt an, ob die Schlüssel Drehung, Skala, Position oder Matrix Schlüssel sind (mit den ganzen Zahlen 0, 1, 2 bzw. 3).</span><span class="sxs-lookup"><span data-stu-id="cc7a6-108">keyType - Specifies whether the keys are rotation, scale, position, or matrix keys (using the integers 0, 1, 2, or 3, respectively).</span></span>
-   <span data-ttu-id="cc7a6-109">nkeys: Anzahl der Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-109">nKeys - Number of keys.</span></span>
-   <span data-ttu-id="cc7a6-110">Keys: ein Array von Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-110">keys - An array of keys.</span></span> <span data-ttu-id="cc7a6-111">Weitere Informationen finden Sie unter [**timedfloatkeys**](timedfloatkeys.md).</span><span class="sxs-lookup"><span data-stu-id="cc7a6-111">See [**TimedFloatKeys**](timedfloatkeys.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc7a6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc7a6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7a6-113">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="cc7a6-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



