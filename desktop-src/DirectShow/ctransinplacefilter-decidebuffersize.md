---
description: 'CTransInPlaceFilter.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen des Ausgabepins fest.'
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: CTransInPlaceFilter.DecideBufferSize-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094828"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="4cd9f-103">CTransInPlaceFilter.DecideBufferSize-Methode</span><span class="sxs-lookup"><span data-stu-id="4cd9f-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="4cd9f-104">Die `DecideBufferSize` -Methode legt die Pufferanforderungen des Ausgabepins fest.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cd9f-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="4cd9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd9f-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="4cd9f-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="4cd9f-108">Zeiger auf das [**IMemAllocator-Objekt,**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) das vom Ausgabepin verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="4cd9f-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="4cd9f-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="4cd9f-110">Zeiger auf die angeforderten Zuweisungseigenschaften für Anzahl, Größe und Ausrichtung, wie von der [**ALLOCATOR \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd9f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cd9f-111">Return value</span></span>

<span data-ttu-id="4cd9f-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4cd9f-113">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4cd9f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4cd9f-114">Return code</span></span>                                                                            | <span data-ttu-id="4cd9f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cd9f-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4cd9f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd9f-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4cd9f-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="4cd9f-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="4cd9f-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd9f-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4cd9f-119">Fehler</span><span class="sxs-lookup"><span data-stu-id="4cd9f-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cd9f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cd9f-120">Remarks</span></span>

<span data-ttu-id="4cd9f-121">Diese Methode wird aufgerufen, wenn die **CTransInPlaceFilter-Klasse** eine Puffergröße für den Downstreamfilter bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="4cd9f-122">Wenn der **CTransInPlaceFilter-Filter** bereits upstream verbunden ist, verwendet er die Zuweisungseigenschaften für die Upstream-Pinverbindung.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="4cd9f-123">Andernfalls wird die Puffergröße als temporärer Platzhalterwert auf 1 Byte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="4cd9f-124">Wenn der Upstreamfilter eine Verbindung herstellt, wird die Downstreamzuweisung von der **CTransInPlaceFilter-Klasse** neu ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="4cd9f-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="4cd9f-125">Weitere Informationen zum Pinverbindungsprozess in dieser Klasse finden Sie unter [**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="4cd9f-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd9f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cd9f-126">Requirements</span></span>



| <span data-ttu-id="4cd9f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cd9f-127">Requirement</span></span> | <span data-ttu-id="4cd9f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4cd9f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd9f-129">Header</span><span class="sxs-lookup"><span data-stu-id="4cd9f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4cd9f-130"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd9f-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4cd9f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cd9f-131">Library</span></span><br/> | <dl> <span data-ttu-id="4cd9f-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd9f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd9f-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4cd9f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd9f-134">**CTransInPlaceFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4cd9f-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




