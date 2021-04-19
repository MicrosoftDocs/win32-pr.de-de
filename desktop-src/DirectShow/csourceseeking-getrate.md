---
description: 'Die getrate-Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die imediaseeking:: getrate-Methode.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Csourceseeking. getrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b14cad0b043193f7ee410455aaa399e3bcb26715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366751"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="c3f0f-104">Csourceseeking. getrate-Methode</span><span class="sxs-lookup"><span data-stu-id="c3f0f-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="c3f0f-105">Die- `GetRate` Methode ruft die Wiedergabe Rate ab.</span><span class="sxs-lookup"><span data-stu-id="c3f0f-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="c3f0f-106">Diese Methode implementiert die [**imediaseeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c3f0f-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f0f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3f0f-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="c3f0f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3f0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f0f-109">*pdrate*</span><span class="sxs-lookup"><span data-stu-id="c3f0f-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f0f-110">Ein Zeiger auf eine Variable, die die Wiedergabe Rate empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3f0f-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f0f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3f0f-111">Return value</span></span>

<span data-ttu-id="c3f0f-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c3f0f-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="c3f0f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c3f0f-113">Return code</span></span>                                                                               | <span data-ttu-id="c3f0f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3f0f-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="c3f0f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f0f-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c3f0f-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="c3f0f-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="c3f0f-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f0f-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c3f0f-118">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="c3f0f-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3f0f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3f0f-119">Remarks</span></span>

<span data-ttu-id="c3f0f-120">Die Wiedergabe Rate wird von der Element Variablen [**csourceseeking:: m \_ drateseeking**](csourceseeking-m-drateseeking.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3f0f-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f0f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3f0f-121">Requirements</span></span>



| <span data-ttu-id="c3f0f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3f0f-122">Requirement</span></span> | <span data-ttu-id="c3f0f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c3f0f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f0f-124">Header</span><span class="sxs-lookup"><span data-stu-id="c3f0f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c3f0f-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f0f-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3f0f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3f0f-126">Library</span></span><br/> | <dl> <span data-ttu-id="c3f0f-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f0f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f0f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3f0f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f0f-129">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c3f0f-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




