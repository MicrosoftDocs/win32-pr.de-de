---
title: Die animationnames-Auflistung
description: Die animationnames-Auflistung
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856168"
---
# <a name="the-animationnames-collection"></a><span data-ttu-id="0413e-103">Die animationnames-Auflistung</span><span class="sxs-lookup"><span data-stu-id="0413e-103">The AnimationNames Collection</span></span>

<span data-ttu-id="0413e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0413e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0413e-105">Die [**animationnames**](https://www.bing.com/search?q=**AnimationNames**) -Auflistung ist eine spezielle Sammlung, die die Liste der für ein Zeichen kompilierten Animations Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="0413e-105">The [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) collection is a special collection that contains the list of animation names compiled for a character.</span></span> <span data-ttu-id="0413e-106">Sie können die Auflistung verwenden, um die Namen der Animationen für ein Zeichen aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="0413e-106">You can use the collection to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="0413e-107">Beispielsweise können Sie in Visual Basic oder VBScript (2,0 oder höher) auf diese Namen mithilfe der **for each-... Nächste** Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="0413e-107">For example, in Visual Basic or VBScript (2.0 or later) you can access these names using the **For Each...Next** statements:</span></span>


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



<span data-ttu-id="0413e-108">Elemente in der Auflistung haben keine Eigenschaften, sodass auf einzelne Elemente nicht direkt zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0413e-108">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span>

<span data-ttu-id="0413e-109">Damit. ACF-Zeichen: die Auflistung gibt alle Animationen zurück, die für das Zeichen definiert wurden, nicht nur diejenigen, die mit der [**Get**](get-method.md) -Methode abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="0413e-109">For .ACF characters, the collection returns all the animations that have been defined for the character, not just the ones that have been retrieved with the [**Get**](get-method.md) method.</span></span>

 

 




