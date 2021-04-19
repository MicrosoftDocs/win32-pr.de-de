---
description: 'Die getallocator-Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin:: getallocator-Methode.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Ctransinplaceinputpin. getallocator-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358307"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="71143-104">Ctransinplaceinputpin. getallocator-Methode</span><span class="sxs-lookup"><span data-stu-id="71143-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="71143-105">Die- `GetAllocator` Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="71143-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="71143-106">Diese Methode implementiert die [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode.</span><span class="sxs-lookup"><span data-stu-id="71143-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71143-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="71143-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="71143-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="71143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71143-109">*ppzuzuweisung*</span><span class="sxs-lookup"><span data-stu-id="71143-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="71143-110">Empfängt einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.</span><span class="sxs-lookup"><span data-stu-id="71143-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71143-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71143-111">Return value</span></span>

<span data-ttu-id="71143-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71143-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71143-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="71143-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="71143-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="71143-114">Return code</span></span>                                                                                          | <span data-ttu-id="71143-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71143-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="71143-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71143-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="71143-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="71143-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="71143-118"><dt>**VFW \_ E \_ No- \_ Zuweisung**</dt></span><span class="sxs-lookup"><span data-stu-id="71143-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="71143-119">Es ist keine Zuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71143-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71143-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71143-120">Remarks</span></span>

<span data-ttu-id="71143-121">Wenn die Ausgabe-PIN des Filters verbunden ist, fordert diese Methode eine Zuweisung aus der Eingabe-PIN des downstreamfilters an.</span><span class="sxs-lookup"><span data-stu-id="71143-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="71143-122">Wenn die Ausgabe-PIN des Filters nicht verbunden ist, erstellt diese Methode eine temporäre Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="71143-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="71143-123">Wenn die Ausgabepin später verbunden ist, stellt der Filter erneut eine Verbindung mit der eingabepin her und verhandelt die Zuweisung erneut.</span><span class="sxs-lookup"><span data-stu-id="71143-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="71143-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71143-124">Requirements</span></span>



| <span data-ttu-id="71143-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71143-125">Requirement</span></span> | <span data-ttu-id="71143-126">Wert</span><span class="sxs-lookup"><span data-stu-id="71143-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71143-127">Header</span><span class="sxs-lookup"><span data-stu-id="71143-127">Header</span></span><br/>  | <dl> <span data-ttu-id="71143-128"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71143-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71143-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71143-129">Library</span></span><br/> | <dl> <span data-ttu-id="71143-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="71143-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71143-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71143-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71143-132">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="71143-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




