---
description: 'CPosPassThru.GetRate-Methode: Die GetRate-Methode ruft die Wiedergaberate ab. Diese Methode implementiert die IMediaSeeking::GetRate-Methode.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: CPosPassThru.GetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085558"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="60b47-104">CPosPassThru.GetRate-Methode</span><span class="sxs-lookup"><span data-stu-id="60b47-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="60b47-105">Die `GetRate` -Methode ruft die Wiedergaberate ab.</span><span class="sxs-lookup"><span data-stu-id="60b47-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="60b47-106">Diese Methode implementiert die [**IMediaSeeking::GetRate-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)</span><span class="sxs-lookup"><span data-stu-id="60b47-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b47-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60b47-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="60b47-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="60b47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b47-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="60b47-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="60b47-110">Zeiger auf eine Variable, die die Wiedergaberate empfängt.</span><span class="sxs-lookup"><span data-stu-id="60b47-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b47-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60b47-111">Return value</span></span>

<span data-ttu-id="60b47-112">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="60b47-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b47-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b47-113">Requirements</span></span>



| <span data-ttu-id="60b47-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b47-114">Requirement</span></span> | <span data-ttu-id="60b47-115">Wert</span><span class="sxs-lookup"><span data-stu-id="60b47-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b47-116">Header</span><span class="sxs-lookup"><span data-stu-id="60b47-116">Header</span></span><br/>  | <dl> <span data-ttu-id="60b47-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="60b47-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60b47-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60b47-118">Library</span></span><br/> | <dl> <span data-ttu-id="60b47-119"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="60b47-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b47-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60b47-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b47-121">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="60b47-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




