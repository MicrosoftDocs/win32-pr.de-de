---
description: 'Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist. Diese Methode überschreibt die cbasepin:: Active-Methode. Wenn die PIN verbunden ist, startet diese Methode den streamingingthread.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Csourcestream. Active-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372432"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="6b748-105">Csourcestream. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="6b748-105">CSourceStream.Active method</span></span>

<span data-ttu-id="6b748-106">Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="6b748-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="6b748-107">Diese Methode überschreibt die [**cbasepin:: Active**](cbasepin-active.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6b748-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="6b748-108">Wenn die PIN verbunden ist, startet diese Methode den streamingingthread.</span><span class="sxs-lookup"><span data-stu-id="6b748-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b748-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b748-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="6b748-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b748-110">Parameters</span></span>

<span data-ttu-id="6b748-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b748-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b748-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b748-112">Return value</span></span>

<span data-ttu-id="6b748-113">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6b748-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6b748-114">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="6b748-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="6b748-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b748-115">Return code</span></span>                                                                             | <span data-ttu-id="6b748-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b748-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="6b748-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6b748-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6b748-118">Die PIN ist bereits aktiv.</span><span class="sxs-lookup"><span data-stu-id="6b748-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="6b748-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b748-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6b748-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6b748-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="6b748-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="6b748-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="6b748-122">Der Thread konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6b748-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6b748-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b748-123">Requirements</span></span>



| <span data-ttu-id="6b748-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b748-124">Requirement</span></span> | <span data-ttu-id="6b748-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6b748-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b748-126">Header</span><span class="sxs-lookup"><span data-stu-id="6b748-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6b748-127"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b748-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6b748-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b748-128">Library</span></span><br/> | <dl> <span data-ttu-id="6b748-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6b748-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b748-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b748-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b748-131">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6b748-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




