---
description: 'Die setpreroll-Methode gibt an, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt. Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden. Diese Methode implementiert die imediasample:: setpreroll-Methode.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Cmediasample. setpreroll-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369416"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="391f0-105">Cmediasample. setpreroll-Methode</span><span class="sxs-lookup"><span data-stu-id="391f0-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="391f0-106">Die- `SetPreroll` Methode gibt an, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt.</span><span class="sxs-lookup"><span data-stu-id="391f0-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="391f0-107">Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="391f0-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="391f0-108">Diese Methode implementiert die [**imediasample:: setpreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) -Methode.</span><span class="sxs-lookup"><span data-stu-id="391f0-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="391f0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="391f0-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="391f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="391f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391f0-111">*bispreroll*</span><span class="sxs-lookup"><span data-stu-id="391f0-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="391f0-112">Boolescher Wert, der angibt, ob es sich um ein vorab Beispiel handelt.</span><span class="sxs-lookup"><span data-stu-id="391f0-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="391f0-113">**True** gibt an, dass es sich um ein vorab Beispiel handelt.</span><span class="sxs-lookup"><span data-stu-id="391f0-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391f0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="391f0-114">Return value</span></span>

<span data-ttu-id="391f0-115">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="391f0-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="391f0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="391f0-116">Remarks</span></span>

<span data-ttu-id="391f0-117">Diese Methode aktualisiert die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die die ein Vorlauf ausgeführt-Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="391f0-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="391f0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="391f0-118">Requirements</span></span>



| <span data-ttu-id="391f0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="391f0-119">Requirement</span></span> | <span data-ttu-id="391f0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="391f0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="391f0-121">Header</span><span class="sxs-lookup"><span data-stu-id="391f0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="391f0-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="391f0-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="391f0-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="391f0-123">Library</span></span><br/> | <dl> <span data-ttu-id="391f0-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="391f0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391f0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="391f0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391f0-126">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="391f0-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




