---
description: 'Die issyncpoint-Methode bestimmt, ob der Anfang des Beispiels ein Synchronisierungs Punkt ist. Diese Methode implementiert die imediasample:: issyncpoint-Methode.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Cmediasample. issyncpoint-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359235"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="ddb2f-104">Cmediasample. issyncpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="ddb2f-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="ddb2f-105">Die- `IsSyncPoint` Methode bestimmt, ob der Anfang des Beispiels ein Synchronisierungs Punkt ist.</span><span class="sxs-lookup"><span data-stu-id="ddb2f-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="ddb2f-106">Diese Methode implementiert die [**imediasample:: issyncpoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ddb2f-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb2f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb2f-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="ddb2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb2f-108">Parameters</span></span>

<span data-ttu-id="ddb2f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ddb2f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddb2f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddb2f-110">Return value</span></span>

<span data-ttu-id="ddb2f-111">Gibt " \_ OK" zurück, wenn das Beispiel ein Synchronisierungs Punkt ist, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="ddb2f-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb2f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddb2f-112">Remarks</span></span>

<span data-ttu-id="ddb2f-113">Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ddb2f-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb2f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddb2f-114">Requirements</span></span>



| <span data-ttu-id="ddb2f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddb2f-115">Requirement</span></span> | <span data-ttu-id="ddb2f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ddb2f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb2f-117">Header</span><span class="sxs-lookup"><span data-stu-id="ddb2f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ddb2f-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb2f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ddb2f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ddb2f-119">Library</span></span><br/> | <dl> <span data-ttu-id="ddb2f-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb2f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb2f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddb2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb2f-122">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ddb2f-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




