---
description: 'Die isdiscontinuity-Methode bestimmt, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die imediasample:: isdiscontinuity-Methode.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Cmediasample. isdiscontinuity-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369394"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="0f1bf-104">Cmediasample. isdiscontinuity-Methode</span><span class="sxs-lookup"><span data-stu-id="0f1bf-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="0f1bf-105">Die- `IsDiscontinuity` Methode bestimmt, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="0f1bf-106">Diese Methode implementiert die [**imediasample:: isdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f1bf-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="0f1bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f1bf-108">Parameters</span></span>

<span data-ttu-id="0f1bf-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f1bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f1bf-110">Return value</span></span>

<span data-ttu-id="0f1bf-111">Gibt "s OK" zurück \_ , wenn das Beispiel eine Unterbrechung im Datenstrom ist, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="0f1bf-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f1bf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f1bf-112">Remarks</span></span>

<span data-ttu-id="0f1bf-113">Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f1bf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f1bf-114">Requirements</span></span>



| <span data-ttu-id="0f1bf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f1bf-115">Requirement</span></span> | <span data-ttu-id="0f1bf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0f1bf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1bf-117">Header</span><span class="sxs-lookup"><span data-stu-id="0f1bf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f1bf-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f1bf-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f1bf-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f1bf-119">Library</span></span><br/> | <dl> <span data-ttu-id="0f1bf-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f1bf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f1bf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f1bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f1bf-122">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f1bf-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




