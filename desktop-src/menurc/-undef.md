---
title: " undef"
description: Mit der Anweisung \ undef wird die aktuelle Definition des angegebenen Namens entfernt. Alle nachfolgenden Vorkommen des Namens werden ohne Ersetzung verarbeitet.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338388"
---
# <a name="undef"></a><span data-ttu-id="529ea-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="529ea-104">\#undef</span></span>

<span data-ttu-id="529ea-105">Mit der **\# undef** -Direktive wird die aktuelle Definition des angegebenen Namens entfernt.</span><span class="sxs-lookup"><span data-stu-id="529ea-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="529ea-106">Alle nachfolgenden Vorkommen des Namens werden ohne Ersetzung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="529ea-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="529ea-107"><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="529ea-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="529ea-108">Der Name, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="529ea-108">Name to be removed.</span></span> <span data-ttu-id="529ea-109">Dieser Wert ist eine beliebige Kombination aus Buchstaben, Ziffern und Interpunktions Zeichen, die für den C/C++-Präprozessor gültig ist.</span><span class="sxs-lookup"><span data-stu-id="529ea-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="529ea-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529ea-110">Example</span></span>

<span data-ttu-id="529ea-111">In diesem Beispiel werden die Definitionen für die Namen "ungleich NULL" und "userclass" entfernt:</span><span class="sxs-lookup"><span data-stu-id="529ea-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="529ea-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="529ea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="529ea-113">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="529ea-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




