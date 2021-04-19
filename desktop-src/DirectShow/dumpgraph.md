---
description: Die dumpgraph-Funktion sendet Informationen über ein Filter Diagramm an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Dumpgraph-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358606"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="dec31-104">Dumpgraph-Funktion</span><span class="sxs-lookup"><span data-stu-id="dec31-104">DumpGraph function</span></span>

<span data-ttu-id="dec31-105">Die- `DumpGraph` Funktion sendet Informationen über ein Filter Diagramm an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="dec31-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="dec31-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dec31-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec31-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="dec31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dec31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec31-109">*PGraph*</span><span class="sxs-lookup"><span data-stu-id="dec31-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="dec31-110">Zeiger auf die [**ifiltergraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) -Schnittstelle im Filter Diagramm-Manager.</span><span class="sxs-lookup"><span data-stu-id="dec31-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="dec31-111">*dwlevel*</span><span class="sxs-lookup"><span data-stu-id="dec31-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="dec31-112">Protokolliergrad.</span><span class="sxs-lookup"><span data-stu-id="dec31-112">Logging level.</span></span> <span data-ttu-id="dec31-113">Die Funktion generiert eine Protokoll \_ Ablaufverfolgungs-Nachricht mit dem angegebenen Protokolliergrad.</span><span class="sxs-lookup"><span data-stu-id="dec31-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec31-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dec31-114">Return value</span></span>

<span data-ttu-id="dec31-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dec31-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec31-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dec31-116">Requirements</span></span>



| <span data-ttu-id="dec31-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dec31-117">Requirement</span></span> | <span data-ttu-id="dec31-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dec31-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec31-119">Header</span><span class="sxs-lookup"><span data-stu-id="dec31-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dec31-120"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dec31-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dec31-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dec31-121">Library</span></span><br/> | <dl> <span data-ttu-id="dec31-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dec31-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec31-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dec31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec31-124">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="dec31-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




