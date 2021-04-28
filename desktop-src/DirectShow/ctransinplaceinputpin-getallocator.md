---
description: 'CTransInPlaceInputPin.GetAllocator-Methode: Die GetAllocator-Methode ruft die von diesem Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin::GetAllocator-Methode.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: CTransInPlaceInputPin.GetAllocator-Methode (Transip.h)
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
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084658"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="e3017-104">CTransInPlaceInputPin.GetAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="e3017-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="e3017-105">Die `GetAllocator` -Methode ruft die von dieser Stecknadel vorgeschlagene Speicherbelegung ab.</span><span class="sxs-lookup"><span data-stu-id="e3017-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="e3017-106">Diese Methode implementiert die [**IMemInputPin::GetAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)</span><span class="sxs-lookup"><span data-stu-id="e3017-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3017-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3017-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="e3017-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3017-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3017-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="e3017-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="e3017-110">Empfängt einen Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="e3017-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3017-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3017-111">Return value</span></span>

<span data-ttu-id="e3017-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="e3017-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e3017-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="e3017-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e3017-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e3017-114">Return code</span></span>                                                                                          | <span data-ttu-id="e3017-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3017-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e3017-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3017-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="e3017-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e3017-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="e3017-118"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="e3017-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="e3017-119">Es ist keine Zuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3017-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3017-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3017-120">Remarks</span></span>

<span data-ttu-id="e3017-121">Wenn der Ausgabepin des Filters verbunden ist, fordert diese Methode eine Zuweisung vom Eingabepin des Downstreamfilters an.</span><span class="sxs-lookup"><span data-stu-id="e3017-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="e3017-122">Wenn der Ausgabepin des Filters nicht verbunden ist, erstellt diese Methode eine temporäre Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="e3017-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="e3017-123">Wenn der Ausgabepin später verbunden ist, verbindet der Filter den Eingabepin erneut und gibt die Zuweisung neu aus.</span><span class="sxs-lookup"><span data-stu-id="e3017-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3017-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3017-124">Requirements</span></span>



| <span data-ttu-id="e3017-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3017-125">Requirement</span></span> | <span data-ttu-id="e3017-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e3017-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3017-127">Header</span><span class="sxs-lookup"><span data-stu-id="e3017-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e3017-128"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3017-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3017-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3017-129">Library</span></span><br/> | <dl> <span data-ttu-id="e3017-130"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e3017-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3017-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e3017-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3017-132">**CTransInPlaceInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e3017-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




