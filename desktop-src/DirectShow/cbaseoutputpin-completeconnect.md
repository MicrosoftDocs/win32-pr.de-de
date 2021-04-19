---
description: Die completeconnect-Methode schließt eine Verbindung mit einer Eingabe-PIN ab.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Cbaseoutputpin. completeconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369124"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="8a2b0-103">Cbaseoutputpin. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="8a2b0-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="8a2b0-104">Die- `CompleteConnect` Methode schließt eine Verbindung mit einer Eingabe-PIN ab.</span><span class="sxs-lookup"><span data-stu-id="8a2b0-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a2b0-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="8a2b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a2b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2b0-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="8a2b0-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="8a2b0-108">Zeiger auf die eingabepin.</span><span class="sxs-lookup"><span data-stu-id="8a2b0-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2b0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a2b0-109">Return value</span></span>

<span data-ttu-id="8a2b0-110">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="8a2b0-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a2b0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a2b0-111">Remarks</span></span>

<span data-ttu-id="8a2b0-112">Diese Methode überschreibt die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8a2b0-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="8a2b0-113">Sie ruft die [**decidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode auf, die die für diese Verbindung zu verwendende Speicherzuweisung auswählt.</span><span class="sxs-lookup"><span data-stu-id="8a2b0-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a2b0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a2b0-114">Requirements</span></span>



| <span data-ttu-id="8a2b0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a2b0-115">Requirement</span></span> | <span data-ttu-id="8a2b0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8a2b0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2b0-117">Header</span><span class="sxs-lookup"><span data-stu-id="8a2b0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8a2b0-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2b0-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8a2b0-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a2b0-119">Library</span></span><br/> | <dl> <span data-ttu-id="8a2b0-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2b0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a2b0-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a2b0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2b0-122">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8a2b0-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




