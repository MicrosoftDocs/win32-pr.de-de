---
title: " define"
description: Die Anweisung \ define weist den angegebenen Wert dem angegebenen Namen zu. Alle nachfolgenden Vorkommen des Namens werden durch den-Wert ersetzt.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711951"
---
# <a name="define"></a><span data-ttu-id="98408-104">\#definieren</span><span class="sxs-lookup"><span data-stu-id="98408-104">\#define</span></span>

<span data-ttu-id="98408-105">Die **\# define** -Direktive weist den angegebenen Wert dem angegebenen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="98408-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="98408-106">Alle nachfolgenden Vorkommen des Namens werden durch den-Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="98408-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="98408-107"><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="98408-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="98408-108">Name, der definiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="98408-108">Name to be defined.</span></span> <span data-ttu-id="98408-109">Dieser Wert ist eine beliebige Kombination aus Buchstaben, Ziffern und Interpunktions Zeichen, die für den C/C++-Präprozessor gültig ist.</span><span class="sxs-lookup"><span data-stu-id="98408-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="98408-110"><span id="value"></span><span id="VALUE"></span>*Wert*</span><span class="sxs-lookup"><span data-stu-id="98408-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="98408-111">Eine ganze Zahl, eine Zeichenfolge oder eine Textzeile.</span><span class="sxs-lookup"><span data-stu-id="98408-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="98408-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="98408-112">Example</span></span>

<span data-ttu-id="98408-113">In diesem Beispiel werden den Namen "Nonzero" und "userclass" Werte zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="98408-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="98408-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98408-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98408-115">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="98408-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




