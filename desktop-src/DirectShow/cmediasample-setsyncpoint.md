---
description: 'Die setsyncpoint-Methode gibt an, ob der Anfang dieses Beispiels ein Synchronisierungs Punkt ist. Diese Methode implementiert die imediasample:: setsyncpoint-Methode.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Cmediasample. setsyncpoint-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352850"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="e7b80-104">Cmediasample. setsyncpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="e7b80-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="e7b80-105">Die- `SetSyncPoint` Methode gibt an, ob der Anfang dieses Beispiels ein Synchronisierungs Punkt ist.</span><span class="sxs-lookup"><span data-stu-id="e7b80-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="e7b80-106">Diese Methode implementiert die [**imediasample:: setsyncpoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e7b80-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b80-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7b80-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="e7b80-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7b80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b80-109">*bissyncpoint*</span><span class="sxs-lookup"><span data-stu-id="e7b80-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b80-110">Boolescher Wert, der angibt, ob es sich um einen Synchronisierungs Punkt handelt.</span><span class="sxs-lookup"><span data-stu-id="e7b80-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="e7b80-111">**True** gibt an, dass dies ein Synchronisierungs Punkt ist.</span><span class="sxs-lookup"><span data-stu-id="e7b80-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b80-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7b80-112">Return value</span></span>

<span data-ttu-id="e7b80-113">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b80-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b80-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7b80-114">Remarks</span></span>

<span data-ttu-id="e7b80-115">Diese Methode aktualisiert die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die die Synchronisierungs Punkt Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="e7b80-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b80-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7b80-116">Requirements</span></span>



| <span data-ttu-id="e7b80-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7b80-117">Requirement</span></span> | <span data-ttu-id="e7b80-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e7b80-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b80-119">Header</span><span class="sxs-lookup"><span data-stu-id="e7b80-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b80-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7b80-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e7b80-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7b80-121">Library</span></span><br/> | <dl> <span data-ttu-id="e7b80-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e7b80-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b80-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7b80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b80-124">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e7b80-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




