---
description: Definiert die Auswirkungen von Gleit Komma Zahlen. Diese Vorlage ersetzt die effectfloat-Vorlage.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: Effectparamfloat
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041185"
---
# <a name="effectparamfloats"></a><span data-ttu-id="e2332-104">Effectparamfloat</span><span class="sxs-lookup"><span data-stu-id="e2332-104">EffectParamFloats</span></span>

<span data-ttu-id="e2332-105">Definiert die Auswirkungen von Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="e2332-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="e2332-106">Diese Vorlage ersetzt die [**effectfloat**](effectfloats.md) -Vorlage.</span><span class="sxs-lookup"><span data-stu-id="e2332-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="e2332-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="e2332-107">Where:</span></span>

-   <span data-ttu-id="e2332-108">ParamName: der Name des Arrays von Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="e2332-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="e2332-109">nfloat: Anzahl von Gleit Komma Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="e2332-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="e2332-110">Schwebt ein \[ nfloat \] -Array von Gleit Komma Werten.</span><span class="sxs-lookup"><span data-stu-id="e2332-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2332-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2332-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2332-112">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="e2332-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



