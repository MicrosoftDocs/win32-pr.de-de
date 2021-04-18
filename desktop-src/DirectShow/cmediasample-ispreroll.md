---
description: 'Die ispreroll-Methode bestimmt, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt. Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden. Diese Methode implementiert die imediasample:: ispreroll-Methode.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Cmediasample. ispreroll-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358241"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="231b0-105">Cmediasample. ispreroll-Methode</span><span class="sxs-lookup"><span data-stu-id="231b0-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="231b0-106">Die- `IsPreroll` Methode bestimmt, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt.</span><span class="sxs-lookup"><span data-stu-id="231b0-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="231b0-107">Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="231b0-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="231b0-108">Diese Methode implementiert die [**imediasample:: ispreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) -Methode.</span><span class="sxs-lookup"><span data-stu-id="231b0-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="231b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="231b0-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="231b0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="231b0-110">Parameters</span></span>

<span data-ttu-id="231b0-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="231b0-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="231b0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="231b0-112">Return value</span></span>

<span data-ttu-id="231b0-113">Gibt "s OK" zurück \_ , wenn es sich bei dem Beispiel um ein vorab Beispiel handelt, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="231b0-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="231b0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="231b0-114">Remarks</span></span>

<span data-ttu-id="231b0-115">Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="231b0-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="231b0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="231b0-116">Requirements</span></span>



| <span data-ttu-id="231b0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="231b0-117">Requirement</span></span> | <span data-ttu-id="231b0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="231b0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="231b0-119">Header</span><span class="sxs-lookup"><span data-stu-id="231b0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="231b0-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="231b0-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="231b0-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="231b0-121">Library</span></span><br/> | <dl> <span data-ttu-id="231b0-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="231b0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="231b0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="231b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231b0-124">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="231b0-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




