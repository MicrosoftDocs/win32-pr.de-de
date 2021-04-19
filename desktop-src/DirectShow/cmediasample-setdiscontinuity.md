---
description: 'Die setdiscontinuity-Methode gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die imediasample:: setdiscontinuity-Methode.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Cmediasample. setdiscontinuity-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352865"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="9f3f9-104">Cmediasample. setdiscontinuity-Methode</span><span class="sxs-lookup"><span data-stu-id="9f3f9-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="9f3f9-105">Die- `SetDiscontinuity` Methode gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt.</span><span class="sxs-lookup"><span data-stu-id="9f3f9-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="9f3f9-106">Diese Methode implementiert die [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9f3f9-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f3f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f3f9-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="9f3f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f3f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f3f9-109">*bdis-Datei*</span><span class="sxs-lookup"><span data-stu-id="9f3f9-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="9f3f9-110">Boolescher Wert, der angibt, ob es sich bei diesem Beispiel um eine Diskontinuität handelt.</span><span class="sxs-lookup"><span data-stu-id="9f3f9-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="9f3f9-111">Wenn der Wert **true** ist, wird das Medien Beispiel mit dem vorherigen Beispiel diskontinuierlich.</span><span class="sxs-lookup"><span data-stu-id="9f3f9-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f3f9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f3f9-112">Return value</span></span>

<span data-ttu-id="9f3f9-113">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9f3f9-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f3f9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f3f9-114">Remarks</span></span>

<span data-ttu-id="9f3f9-115">Diese Methode aktualisiert die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die die Diskontinuität-Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="9f3f9-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f3f9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f3f9-116">Requirements</span></span>



| <span data-ttu-id="9f3f9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f3f9-117">Requirement</span></span> | <span data-ttu-id="9f3f9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9f3f9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3f9-119">Header</span><span class="sxs-lookup"><span data-stu-id="9f3f9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9f3f9-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f3f9-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f3f9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f3f9-121">Library</span></span><br/> | <dl> <span data-ttu-id="9f3f9-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9f3f9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f3f9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f3f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f3f9-124">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f3f9-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




