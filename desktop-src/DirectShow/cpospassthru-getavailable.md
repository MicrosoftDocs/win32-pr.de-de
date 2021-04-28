---
description: 'CPosPassThru.GetAvailable-Methode: Die GetAvailable-Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind. Diese Methode implementiert die IMediaSeeking::GetAvailable-Methode.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: CPosPassThru.GetAvailable-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d56827a68f4c287e5808f0d8f64b8142c31b1f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095288"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="8a11c-104">CPosPassThru.GetAvailable-Methode</span><span class="sxs-lookup"><span data-stu-id="8a11c-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="8a11c-105">Die `GetAvailable` -Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind.</span><span class="sxs-lookup"><span data-stu-id="8a11c-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="8a11c-106">Diese Methode implementiert die [**IMediaSeeking::GetAvailable-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)</span><span class="sxs-lookup"><span data-stu-id="8a11c-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a11c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a11c-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="8a11c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a11c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a11c-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="8a11c-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="8a11c-110">Zeiger auf eine Variable, die die früheste Zeit für effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="8a11c-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="8a11c-111">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="8a11c-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="8a11c-112">Zeiger auf eine Variable, die die letzte Zeit für effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="8a11c-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a11c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a11c-113">Return value</span></span>

<span data-ttu-id="8a11c-114">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="8a11c-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a11c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a11c-115">Requirements</span></span>



| <span data-ttu-id="8a11c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a11c-116">Requirement</span></span> | <span data-ttu-id="8a11c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8a11c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a11c-118">Header</span><span class="sxs-lookup"><span data-stu-id="8a11c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8a11c-119"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a11c-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8a11c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a11c-120">Library</span></span><br/> | <dl> <span data-ttu-id="8a11c-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8a11c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a11c-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8a11c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a11c-123">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8a11c-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




