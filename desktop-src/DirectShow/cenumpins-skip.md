---
description: 'Die Skip-Methode überspringt eine angegebene Anzahl von Pins in der enumerationssequenz. Diese Methode implementiert die iumumpins:: Skip-Methode.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Cenumpins. Skip-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372590"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="aa652-104">Cenumpins. Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="aa652-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="aa652-105">Die- `Skip` Methode überspringt eine angegebene Anzahl von Pins in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="aa652-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="aa652-106">Diese Methode implementiert die [**iumumpins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) -Methode.</span><span class="sxs-lookup"><span data-stu-id="aa652-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa652-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa652-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="aa652-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa652-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa652-109">*cpins*</span><span class="sxs-lookup"><span data-stu-id="aa652-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="aa652-110">Anzahl der Pins, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aa652-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa652-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa652-111">Return value</span></span>

<span data-ttu-id="aa652-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="aa652-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="aa652-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="aa652-113">Return code</span></span>                                                                                                | <span data-ttu-id="aa652-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa652-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa652-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="aa652-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="aa652-116">Wird über das Ende der Sequenz übersprungen.</span><span class="sxs-lookup"><span data-stu-id="aa652-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="aa652-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa652-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="aa652-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="aa652-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="aa652-119"><dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt></span><span class="sxs-lookup"><span data-stu-id="aa652-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="aa652-120">Der Zustand des Filters wurde geändert und ist nun inkonsistent mit dem Enumerator.</span><span class="sxs-lookup"><span data-stu-id="aa652-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa652-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa652-121">Requirements</span></span>



| <span data-ttu-id="aa652-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa652-122">Requirement</span></span> | <span data-ttu-id="aa652-123">Wert</span><span class="sxs-lookup"><span data-stu-id="aa652-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa652-124">Header</span><span class="sxs-lookup"><span data-stu-id="aa652-124">Header</span></span><br/>  | <dl> <span data-ttu-id="aa652-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa652-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aa652-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa652-126">Library</span></span><br/> | <dl> <span data-ttu-id="aa652-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aa652-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa652-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa652-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa652-129">**Cenumpins-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aa652-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




