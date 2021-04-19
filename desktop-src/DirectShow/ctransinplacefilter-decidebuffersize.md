---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Ctransinplacefilter. decidebuffersize-Methode (transip. h)
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
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373683"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="20fbf-103">Ctransinplacefilter. decidebuffersize-Methode</span><span class="sxs-lookup"><span data-stu-id="20fbf-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="20fbf-104">Die `DecideBufferSize` -Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.</span><span class="sxs-lookup"><span data-stu-id="20fbf-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fbf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20fbf-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="20fbf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20fbf-107">*palloc*</span><span class="sxs-lookup"><span data-stu-id="20fbf-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="20fbf-108">Zeiger auf das [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Objekt, das von der Ausgabe-PIN verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20fbf-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="20fbf-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="20fbf-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="20fbf-110">Zeiger auf die angeforderten Zuweisungs Eigenschaften für Anzahl, Größe und Ausrichtung, wie in der [**Zuweisungs \_ Eigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="20fbf-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20fbf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20fbf-111">Return value</span></span>

<span data-ttu-id="20fbf-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20fbf-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="20fbf-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="20fbf-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="20fbf-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="20fbf-114">Return code</span></span>                                                                            | <span data-ttu-id="20fbf-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20fbf-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="20fbf-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20fbf-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="20fbf-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="20fbf-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="20fbf-118"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="20fbf-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="20fbf-119">Fehler</span><span class="sxs-lookup"><span data-stu-id="20fbf-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20fbf-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20fbf-120">Remarks</span></span>

<span data-ttu-id="20fbf-121">Diese Methode wird aufgerufen, wenn die **ctransinplacefilter** -Klasse eine Puffergröße für den downstreamfilter bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="20fbf-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="20fbf-122">Wenn der **ctransinplacefilter** -Filter bereits mit Upstream verbunden ist, werden die zuordnereigenschaften in der Upstream-Pin-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="20fbf-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="20fbf-123">Andernfalls wird die Puffergröße als temporärer Platzhalter Wert auf 1 Byte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="20fbf-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="20fbf-124">Wenn der upstreamfilter eine Verbindung herstellt, wird die Downstream-Zuweisung von der **ctransinplacefilter** -Klasse erneut ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="20fbf-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="20fbf-125">Weitere Informationen zum Pin-Verbindungsprozess in dieser Klasse finden Sie unter [**ctransinplacefilter-Klasse**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="20fbf-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20fbf-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20fbf-126">Requirements</span></span>



| <span data-ttu-id="20fbf-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20fbf-127">Requirement</span></span> | <span data-ttu-id="20fbf-128">Wert</span><span class="sxs-lookup"><span data-stu-id="20fbf-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fbf-129">Header</span><span class="sxs-lookup"><span data-stu-id="20fbf-129">Header</span></span><br/>  | <dl> <span data-ttu-id="20fbf-130"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20fbf-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20fbf-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20fbf-131">Library</span></span><br/> | <dl> <span data-ttu-id="20fbf-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="20fbf-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fbf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20fbf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fbf-134">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="20fbf-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




