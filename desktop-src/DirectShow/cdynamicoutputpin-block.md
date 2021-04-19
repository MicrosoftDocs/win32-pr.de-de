---
description: 'Die Block-Methode blockiert oder entsperrt den Datenfluss aus der PIN. Diese Methode implementiert die IPinFlowControl:: Block-Methode.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Cdynamicoutputpin. Block-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370847"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="c931a-104">Cdynamicoutputpin. Block-Methode</span><span class="sxs-lookup"><span data-stu-id="c931a-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="c931a-105">Die- `Block` Methode blockiert bzw. entsperrt den Datenfluss aus der PIN.</span><span class="sxs-lookup"><span data-stu-id="c931a-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="c931a-106">Diese Methode implementiert die [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c931a-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c931a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c931a-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="c931a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c931a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c931a-109">*dwblockflags*</span><span class="sxs-lookup"><span data-stu-id="c931a-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c931a-110">Flag, das angibt, ob die PIN blockiert oder freizugeben ist.</span><span class="sxs-lookup"><span data-stu-id="c931a-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="c931a-111">Dies muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="c931a-111">Must be one of the following values:</span></span>

<span data-ttu-id="c931a-112">Zero: entsperrt den Datenfluss von der PIN.</span><span class="sxs-lookup"><span data-stu-id="c931a-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="c931a-113">AM \_ Pin- \_ Fluss \_ Steuerungs \_ Block: blockiert den Datenfluss von der PIN.</span><span class="sxs-lookup"><span data-stu-id="c931a-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="c931a-114">*hevent*</span><span class="sxs-lookup"><span data-stu-id="c931a-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="c931a-115">Handle für ein Ereignis Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="c931a-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c931a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c931a-116">Return value</span></span>

<span data-ttu-id="c931a-117">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c931a-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c931a-118">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c931a-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c931a-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c931a-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="c931a-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c931a-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c931a-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="c931a-122">Die Blockierung der PIN wurde bereits aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="c931a-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="c931a-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="c931a-124">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c931a-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c931a-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="c931a-126">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="c931a-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="c931a-127"><dt>**VFW \_ E \_ Pin \_ bereits \_ blockiert**</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="c931a-128">Die PIN ist bereits in einem anderen Thread blockiert.</span><span class="sxs-lookup"><span data-stu-id="c931a-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="c931a-129"><dt>**VFW \_ E \_ Pin \_ ist \_ \_ in \_ diesem \_ Thread bereits blockiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="c931a-130">Die PIN ist bereits im aufrufenden Thread blockiert.</span><span class="sxs-lookup"><span data-stu-id="c931a-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c931a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c931a-131">Remarks</span></span>

<span data-ttu-id="c931a-132">Weitere Informationen zu dieser Methode finden Sie unter [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span><span class="sxs-lookup"><span data-stu-id="c931a-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="c931a-133">Intern ruft diese Methode eine der folgenden geschützten Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="c931a-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="c931a-134">Block (Asynchronous): [ **cdynamicoutputpin:: asynchronousblockoutputpin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="c931a-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="c931a-135">Block (synchron): [ **cdynamicoutputpin:: synchronousblockoutputpin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="c931a-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="c931a-136">Unblock: [ **cdynamicoutputpin:: unblockoutputpin**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="c931a-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="c931a-137">Das Aufheben der Blockierung erfolgt immer synchron.</span><span class="sxs-lookup"><span data-stu-id="c931a-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c931a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c931a-138">Requirements</span></span>



| <span data-ttu-id="c931a-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c931a-139">Requirement</span></span> | <span data-ttu-id="c931a-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c931a-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c931a-141">Header</span><span class="sxs-lookup"><span data-stu-id="c931a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="c931a-142"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c931a-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c931a-143">Library</span></span><br/> | <dl> <span data-ttu-id="c931a-144">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c931a-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c931a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c931a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c931a-146">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c931a-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




