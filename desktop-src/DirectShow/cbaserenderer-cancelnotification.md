---
description: Die cancelnotification-Methode bricht das Timer-Ereignis ab, das das Rendering plant.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Cbaserderderer. cancelnotification-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361313"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="21d3e-103">Cbaserderderer. cancelnotification-Methode</span><span class="sxs-lookup"><span data-stu-id="21d3e-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="21d3e-104">Die- `CancelNotification` Methode bricht das Timer-Ereignis ab, das das Rendering plant.</span><span class="sxs-lookup"><span data-stu-id="21d3e-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d3e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21d3e-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="21d3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21d3e-106">Parameters</span></span>

<span data-ttu-id="21d3e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="21d3e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21d3e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21d3e-108">Return value</span></span>

<span data-ttu-id="21d3e-109">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="21d3e-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="21d3e-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="21d3e-110">Return code</span></span>                                                                             | <span data-ttu-id="21d3e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21d3e-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="21d3e-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="21d3e-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="21d3e-113">Es war kein ausstehendes Timer-Ereignis vorhanden.</span><span class="sxs-lookup"><span data-stu-id="21d3e-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="21d3e-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21d3e-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="21d3e-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="21d3e-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="21d3e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21d3e-116">Remarks</span></span>

<span data-ttu-id="21d3e-117">Der Filter ruft diese Methode auf, wenn das Streaming beendet wird.</span><span class="sxs-lookup"><span data-stu-id="21d3e-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="21d3e-118">Die-Methode bricht alle geplanten Renderingvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="21d3e-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d3e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21d3e-119">Requirements</span></span>



| <span data-ttu-id="21d3e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21d3e-120">Requirement</span></span> | <span data-ttu-id="21d3e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="21d3e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21d3e-122">Header</span><span class="sxs-lookup"><span data-stu-id="21d3e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="21d3e-123"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21d3e-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21d3e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21d3e-124">Library</span></span><br/> | <dl> <span data-ttu-id="21d3e-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="21d3e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21d3e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21d3e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d3e-127">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="21d3e-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




