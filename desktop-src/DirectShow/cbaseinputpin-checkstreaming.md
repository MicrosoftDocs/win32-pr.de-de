---
description: Bestimmt, ob die PIN Beispiele annehmen kann.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Cbaseinputpin. checkstreaming-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355260"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="b2f72-103">Cbaseinputpin. checkstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="b2f72-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="b2f72-104">Bestimmt, ob die PIN Beispiele annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="b2f72-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f72-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="b2f72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2f72-106">Parameters</span></span>

<span data-ttu-id="b2f72-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2f72-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2f72-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2f72-108">Return value</span></span>

<span data-ttu-id="b2f72-109">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b2f72-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="b2f72-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b2f72-110">Return code</span></span>                                                                                           | <span data-ttu-id="b2f72-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2f72-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b2f72-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f72-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="b2f72-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b2f72-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="b2f72-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f72-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="b2f72-115">Die PIN wird zurzeit geleert.</span><span class="sxs-lookup"><span data-stu-id="b2f72-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="b2f72-116"><dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f72-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="b2f72-117">Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="b2f72-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="b2f72-118"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f72-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="b2f72-119">Die PIN wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="b2f72-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="b2f72-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f72-120">Remarks</span></span>

<span data-ttu-id="b2f72-121">Die abgeleitete Klasse kann diese Methode überschreiben, um weitere Überprüfungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b2f72-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="b2f72-122">In der über schreibenden Methode wird auch die Basisklassen Implementierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b2f72-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="b2f72-123">Die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b2f72-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="b2f72-124">Sie sollten auch die [**cbasepin:: EndOfStream**](cbasepin-endofstream.md) -Methode überschreiben, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b2f72-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f72-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2f72-125">Requirements</span></span>



| <span data-ttu-id="b2f72-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2f72-126">Requirement</span></span> | <span data-ttu-id="b2f72-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b2f72-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f72-128">Header</span><span class="sxs-lookup"><span data-stu-id="b2f72-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b2f72-129"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f72-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2f72-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2f72-130">Library</span></span><br/> | <dl> <span data-ttu-id="b2f72-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f72-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f72-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2f72-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f72-133">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b2f72-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




