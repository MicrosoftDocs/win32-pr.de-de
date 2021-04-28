---
description: 'CPosPassThru.SetRate-Methode: Die SetRate-Methode legt die Wiedergaberate fest. Diese Methode implementiert die IMediaSeeking::SetRate-Methode.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: CPosPassThru.SetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095218"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="30a98-104">CPosPassThru.SetRate-Methode</span><span class="sxs-lookup"><span data-stu-id="30a98-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="30a98-105">Die `SetRate` -Methode legt die Wiedergaberate fest.</span><span class="sxs-lookup"><span data-stu-id="30a98-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="30a98-106">Diese Methode implementiert die [**IMediaSeeking::SetRate-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)</span><span class="sxs-lookup"><span data-stu-id="30a98-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a98-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a98-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="30a98-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a98-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="30a98-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="30a98-110">Wiedergaberate.</span><span class="sxs-lookup"><span data-stu-id="30a98-110">Playback rate.</span></span> <span data-ttu-id="30a98-111">Darf nicht 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="30a98-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a98-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30a98-112">Return value</span></span>

<span data-ttu-id="30a98-113">Gibt E \_ INVALIDARG zurück, wenn *dRate* 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="30a98-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="30a98-114">Andernfalls wird der **HRESULT-Wert** vom verbundenen Pin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30a98-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a98-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30a98-115">Requirements</span></span>



| <span data-ttu-id="30a98-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30a98-116">Requirement</span></span> | <span data-ttu-id="30a98-117">Wert</span><span class="sxs-lookup"><span data-stu-id="30a98-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a98-118">Header</span><span class="sxs-lookup"><span data-stu-id="30a98-118">Header</span></span><br/>  | <dl> <span data-ttu-id="30a98-119"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="30a98-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30a98-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30a98-120">Library</span></span><br/> | <dl> <span data-ttu-id="30a98-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="30a98-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a98-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="30a98-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a98-123">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="30a98-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




