---
description: 'CPosPassThru.SetTimeFormat-Methode: Die SetTimeFormat-Methode legt das Zeitformat fest. Diese Methode implementiert die IMediaSeeking::SetTimeFormat-Methode.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: CPosPassThru.SetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81798ccbb51056353c62cd94f821b3567d78a484
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085468"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="a7b78-104">CPosPassThru.SetTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="a7b78-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="a7b78-105">Die SetTimeFormat-Methode legt das Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="a7b78-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="a7b78-106">Diese Methode implementiert die [**IMediaSeeking::SetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)</span><span class="sxs-lookup"><span data-stu-id="a7b78-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b78-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7b78-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a7b78-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7b78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b78-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="a7b78-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b78-110">Zeiger auf eine GUID im Zeitformat.</span><span class="sxs-lookup"><span data-stu-id="a7b78-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b78-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7b78-111">Return value</span></span>

<span data-ttu-id="a7b78-112">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="a7b78-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b78-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7b78-113">Requirements</span></span>



| <span data-ttu-id="a7b78-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7b78-114">Requirement</span></span> | <span data-ttu-id="a7b78-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a7b78-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b78-116">Header</span><span class="sxs-lookup"><span data-stu-id="a7b78-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a7b78-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7b78-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7b78-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7b78-118">Library</span></span><br/> | <dl> <span data-ttu-id="a7b78-119"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a7b78-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b78-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a7b78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b78-121">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a7b78-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="a7b78-122">**Zeitformat-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="a7b78-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




