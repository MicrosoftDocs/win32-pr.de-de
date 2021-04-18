---
description: Die getstddev-Methode schätzt die Standardabweichung in Millisekunden zwischen dem Zeitpunkt, an dem jeder Frame fällig ist, und dem Zeitpunkt, zu dem er tatsächlich gerendert wird, für Statistiken pro Frame.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Cbasevideorenderer. getstddev-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358009"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="20be3-103">Cbasevideorenderer. getstddev-Methode</span><span class="sxs-lookup"><span data-stu-id="20be3-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="20be3-104">Die `GetStdDev` -Methode schätzt die Standardabweichung in Millisekunden zwischen dem Zeitpunkt, an dem jeder Frame fällig ist, und dem tatsächlichen Rendering für pro-Frame-Statistik.</span><span class="sxs-lookup"><span data-stu-id="20be3-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="20be3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20be3-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="20be3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20be3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20be3-107">*nsamples*</span><span class="sxs-lookup"><span data-stu-id="20be3-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="20be3-108">Ganzzahliger Wert, der die Anzahl der Videobeispiele enthält, die vom Videorenderer empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="20be3-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="20be3-109">*piresult*</span><span class="sxs-lookup"><span data-stu-id="20be3-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="20be3-110">Ein Zeiger auf einen ganzzahligen Wert, der die Standardabweichung enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="20be3-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="20be3-111">*llsumsq*</span><span class="sxs-lookup"><span data-stu-id="20be3-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="20be3-112">Ein Wert, der die Standardabweichung aller gerenderten Videobeispiele in Millisekunden darstellt.</span><span class="sxs-lookup"><span data-stu-id="20be3-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="20be3-113">Je niedriger der Wert, desto konsistent ist das Rendering.</span><span class="sxs-lookup"><span data-stu-id="20be3-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="20be3-114">*itot*</span><span class="sxs-lookup"><span data-stu-id="20be3-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="20be3-115">Ein Wert, der den Mittelwert (in Millisekunden) zwischen der gestempelten Zeit und der gerenderten Zeit für alle gerenderten Videobeispiele darstellt.</span><span class="sxs-lookup"><span data-stu-id="20be3-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20be3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20be3-116">Return value</span></span>

<span data-ttu-id="20be3-117">Gibt noError zurück.</span><span class="sxs-lookup"><span data-stu-id="20be3-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="20be3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20be3-118">Requirements</span></span>



| <span data-ttu-id="20be3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20be3-119">Requirement</span></span> | <span data-ttu-id="20be3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="20be3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20be3-121">Header</span><span class="sxs-lookup"><span data-stu-id="20be3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="20be3-122"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20be3-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20be3-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20be3-123">Library</span></span><br/> | <dl> <span data-ttu-id="20be3-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="20be3-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20be3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20be3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20be3-126">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="20be3-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




