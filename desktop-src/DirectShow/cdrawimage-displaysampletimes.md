---
description: Die displaysampletimes-Methode zeichnet die Zeitstempel eines Medien Beispiels oberhalb des Video Bilds.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Cdrawimage. displaysampletimes-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352169"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="02c11-103">Cdrawimage. displaysampletimes-Methode</span><span class="sxs-lookup"><span data-stu-id="02c11-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="02c11-104">Die- `DisplaySampleTimes` Methode zeichnet die Zeitstempel eines Medien Beispiels oberhalb des Video Bilds.</span><span class="sxs-lookup"><span data-stu-id="02c11-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02c11-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="02c11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c11-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="02c11-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="02c11-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="02c11-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c11-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02c11-109">Return value</span></span>

<span data-ttu-id="02c11-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="02c11-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02c11-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02c11-111">Remarks</span></span>

<span data-ttu-id="02c11-112">Diese Methode wird nur in Debugbuilds aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="02c11-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c11-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02c11-113">Requirements</span></span>



| <span data-ttu-id="02c11-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02c11-114">Requirement</span></span> | <span data-ttu-id="02c11-115">Wert</span><span class="sxs-lookup"><span data-stu-id="02c11-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c11-116">Header</span><span class="sxs-lookup"><span data-stu-id="02c11-116">Header</span></span><br/>  | <dl> <span data-ttu-id="02c11-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02c11-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02c11-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02c11-118">Library</span></span><br/> | <dl> <span data-ttu-id="02c11-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="02c11-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c11-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02c11-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c11-121">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="02c11-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




