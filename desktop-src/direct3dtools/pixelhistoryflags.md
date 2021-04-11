---
description: Eine Enumeration, die Flags enthält, die zum Beschreiben eines Pixel Verlaufs Ergebnisses verwendet werden. Siehe pixelhistoryoperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelhistoryflags-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124159"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="1a88d-104"><span id="vspixengine.pixelhistoryflags"></span>Pixelhistoryflags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1a88d-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="1a88d-105">Eine Enumeration, die Flags enthält, die zum Beschreiben eines Pixel Verlaufs Ergebnisses verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a88d-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="1a88d-106">Siehe pixelhistoryoperation.</span><span class="sxs-lookup"><span data-stu-id="1a88d-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a88d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a88d-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="1a88d-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1a88d-108">Constants</span></span>

<span data-ttu-id="1a88d-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF- \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="1a88d-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="1a88d-110">Ein Flag, das dem Anfangs Farbwert (vor dem Frame) entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a88d-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="1a88d-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="1a88d-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="1a88d-112">Ein Flag, das dem klaren Farbergebnis entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a88d-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="1a88d-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF- \_ Zeichnen**</span><span class="sxs-lookup"><span data-stu-id="1a88d-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="1a88d-114">Ein Flag, das dem Ergebnis der Zeichnungs Farbe entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a88d-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="1a88d-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ finalvalue**</span><span class="sxs-lookup"><span data-stu-id="1a88d-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="1a88d-116">Ein Flag, das dem Endergebnis der endgültigen Farbe entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a88d-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="1a88d-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ hascolor**</span><span class="sxs-lookup"><span data-stu-id="1a88d-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="1a88d-118">Ein Flag, das entspricht, ob das Farbergebnis in der pixelhistoryoperation-Struktur vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a88d-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="1a88d-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ hasbcolor**</span><span class="sxs-lookup"><span data-stu-id="1a88d-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="1a88d-120">Ein Flag, das entspricht, ob das endgültige Puffer Farbergebnis in der pixelhistoryoperation-Struktur vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a88d-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="1a88d-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="1a88d-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="1a88d-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ vertexprocessingskipped**</span><span class="sxs-lookup"><span data-stu-id="1a88d-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="1a88d-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a88d-123">Not used.</span></span>

<span data-ttu-id="1a88d-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ modifyresource**</span><span class="sxs-lookup"><span data-stu-id="1a88d-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="1a88d-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ cannotrunfulldepthstenciltest**</span><span class="sxs-lookup"><span data-stu-id="1a88d-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="1a88d-126">Ein Flag, das entspricht, dass es nicht möglich ist, den tiefen-oder Schablonen Test auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1a88d-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a88d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a88d-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1a88d-128">Header</span><span class="sxs-lookup"><span data-stu-id="1a88d-128">Header</span></span></p></td><td><span data-ttu-id="1a88d-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1a88d-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



