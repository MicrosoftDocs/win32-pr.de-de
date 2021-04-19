---
description: 'Die unempfehlung-Methode entfernt eine ausstehende Benachrichtigungs Anforderung. Diese Methode implementiert die IReferenceClock:: unberatungsmethode.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Cbasereferenceclock. unempfehlung-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372702"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="d6560-104">Cbasereferenceclock. unempfehlung-Methode</span><span class="sxs-lookup"><span data-stu-id="d6560-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="d6560-105">Die- `Unadvise` Methode entfernt eine ausstehende Benachrichtigungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6560-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="d6560-106">Diese Methode implementiert die [**IReferenceClock:: unberatungsmethode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .</span><span class="sxs-lookup"><span data-stu-id="d6560-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6560-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6560-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="d6560-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6560-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6560-109">*dwadviabtoken*</span><span class="sxs-lookup"><span data-stu-id="d6560-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="d6560-110">Der Bezeichner der zu entfernenden Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6560-110">Identifier of the request to remove.</span></span> <span data-ttu-id="d6560-111">Verwenden Sie den Wert, der von den Methoden [**cbasereferenceclock:: advientime**](cbasereferenceclock-advisetime.md) oder [**cbasereferenceclock:: advi\periodisch**](cbasereferenceclock-adviseperiodic.md) im *pdwadvictoken* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6560-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6560-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6560-112">Return value</span></span>

<span data-ttu-id="d6560-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d6560-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d6560-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d6560-114">Return code</span></span>                                                                             | <span data-ttu-id="d6560-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6560-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="d6560-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d6560-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d6560-117">Nicht gefunden:</span><span class="sxs-lookup"><span data-stu-id="d6560-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="d6560-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6560-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d6560-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d6560-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d6560-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6560-120">Requirements</span></span>



| <span data-ttu-id="d6560-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6560-121">Requirement</span></span> | <span data-ttu-id="d6560-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d6560-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6560-123">Header</span><span class="sxs-lookup"><span data-stu-id="d6560-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d6560-124"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6560-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6560-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6560-125">Library</span></span><br/> | <dl> <span data-ttu-id="d6560-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d6560-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6560-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6560-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6560-128">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d6560-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




