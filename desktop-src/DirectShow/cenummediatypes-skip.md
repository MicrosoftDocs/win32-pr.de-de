---
description: 'Die Skip-Methode überspringt eine angegebene Anzahl von Medientypen. Diese Methode implementiert die ienummediatypes:: Skip-Methode.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Cenumschlag mediatypes. Skip-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354665"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="78920-104">Cenumschlag mediatypes. Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="78920-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="78920-105">Die- `Skip` Methode überspringt eine angegebene Anzahl von Medientypen.</span><span class="sxs-lookup"><span data-stu-id="78920-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="78920-106">Diese Methode implementiert die [**ienummediatypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) -Methode.</span><span class="sxs-lookup"><span data-stu-id="78920-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78920-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78920-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="78920-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78920-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78920-109">*cmediatypes*</span><span class="sxs-lookup"><span data-stu-id="78920-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="78920-110">Anzahl der zu über springenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="78920-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78920-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78920-111">Return value</span></span>

<span data-ttu-id="78920-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="78920-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="78920-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="78920-113">Return code</span></span>                                                                                                | <span data-ttu-id="78920-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78920-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78920-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="78920-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="78920-116">Wird über das Ende der Sequenz übersprungen.</span><span class="sxs-lookup"><span data-stu-id="78920-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="78920-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78920-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="78920-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="78920-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="78920-119"><dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt></span><span class="sxs-lookup"><span data-stu-id="78920-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="78920-120">Der Zustand der PIN wurde geändert und ist nun inkonsistent mit dem Enumerator.</span><span class="sxs-lookup"><span data-stu-id="78920-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="78920-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78920-121">Requirements</span></span>



| <span data-ttu-id="78920-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78920-122">Requirement</span></span> | <span data-ttu-id="78920-123">Wert</span><span class="sxs-lookup"><span data-stu-id="78920-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78920-124">Header</span><span class="sxs-lookup"><span data-stu-id="78920-124">Header</span></span><br/>  | <dl> <span data-ttu-id="78920-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78920-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78920-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78920-126">Library</span></span><br/> | <dl> <span data-ttu-id="78920-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78920-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78920-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78920-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78920-129">**Cenum mediatypes-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78920-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




