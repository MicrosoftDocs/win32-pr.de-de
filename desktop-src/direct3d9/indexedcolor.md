---
description: Besteht aus einem Index Parameter und einer RGBA-Farbe und wird zum Definieren von Gitter Scheitelpunkt Farben verwendet. Der Index definiert den Scheitelpunkt, auf den die Farbe angewendet wird.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: Indexedcolor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341708"
---
# <a name="indexedcolor"></a><span data-ttu-id="b6f07-104">Indexedcolor</span><span class="sxs-lookup"><span data-stu-id="b6f07-104">IndexedColor</span></span>

<span data-ttu-id="b6f07-105">Besteht aus einem Index Parameter und einer RGBA-Farbe und wird zum Definieren von Gitter Scheitelpunkt Farben verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6f07-105">Consists of an index parameter and an RGBA color and is used for defining mesh vertex colors.</span></span> <span data-ttu-id="b6f07-106">Der Index definiert den Scheitelpunkt, auf den die Farbe angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6f07-106">The index defines the vertex to which the color is applied.</span></span>

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

<span data-ttu-id="b6f07-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="b6f07-107">Where:</span></span>

-   <span data-ttu-id="b6f07-108">Index-A DWORD.</span><span class="sxs-lookup"><span data-stu-id="b6f07-108">index - A DWORD.</span></span> <span data-ttu-id="b6f07-109">Siehe oben genannte Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b6f07-109">See the description above.</span></span>
-   <span data-ttu-id="b6f07-110">indexcolor: eine colorrgba-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="b6f07-110">indexColor - A ColorRGBA template.</span></span> <span data-ttu-id="b6f07-111">Siehe [**colorrgba**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="b6f07-111">See [**ColorRGBA**](colorrgba.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b6f07-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6f07-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f07-113">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b6f07-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



