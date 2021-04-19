---
description: 'Die joinfiltergraph-Methode benachrichtigt den Filter, dass ein Filter Diagramm verknüpft oder Links ist. Diese Methode implementiert die ibasefilter:: joinfiltergraph-Methode.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Cbasefilter. joinfiltergraph-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367754"
---
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="702c6-104">Cbasefilter. joinfiltergraph-Methode</span><span class="sxs-lookup"><span data-stu-id="702c6-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="702c6-105">Mit der- `JoinFilterGraph` Methode wird der Filter benachrichtigt, dass ein Filter Diagramm verknüpft oder Links ist.</span><span class="sxs-lookup"><span data-stu-id="702c6-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="702c6-106">Diese Methode implementiert die [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode.</span><span class="sxs-lookup"><span data-stu-id="702c6-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="702c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="702c6-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="702c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="702c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="702c6-109">*PGraph*</span><span class="sxs-lookup"><span data-stu-id="702c6-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="702c6-110">Ein Zeiger auf die [**ifiltergraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) -Schnittstelle des Filter Diagramm-Managers oder **null** , wenn der Filter das Diagramm verlässt.</span><span class="sxs-lookup"><span data-stu-id="702c6-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="702c6-111">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="702c6-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702c6-112">Ein Zeiger auf eine Unicode-Zeichenfolge, die einen Namen für den Filter enthält.</span><span class="sxs-lookup"><span data-stu-id="702c6-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="702c6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="702c6-113">Return value</span></span>

<span data-ttu-id="702c6-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="702c6-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="702c6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="702c6-115">Remarks</span></span>

<span data-ttu-id="702c6-116">Diese Methode legt die [**cbasefilter:: m \_ PGraph**](cbasefilter-m-pgraph.md) -Member-Variable auf den *PGraph* -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="702c6-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="702c6-117">Außerdem wird ein [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstellen Zeiger abgefragt und in der [**cbasefilter:: m \_ psink**](cbasefilter-m-psink.md) -Element Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="702c6-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="702c6-118">Der Filter behält jedoch keinen Verweis Zähler für eine dieser Schnittstellen bei.</span><span class="sxs-lookup"><span data-stu-id="702c6-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="702c6-119">Dies würde einen Zirkel Verweis Zähler erzeugen, da der Filter Graph-Manager einen Verweis Zähler für den Filter beibehält.</span><span class="sxs-lookup"><span data-stu-id="702c6-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="702c6-120">Die-Methode kopiert die durch " *PName* " angegebene Zeichenfolge in die " [**cbasefilter:: m \_ PName**](cbasefilter-m-pname.md) "-Member-Variable.</span><span class="sxs-lookup"><span data-stu-id="702c6-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="702c6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="702c6-121">Requirements</span></span>



| <span data-ttu-id="702c6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="702c6-122">Requirement</span></span> | <span data-ttu-id="702c6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="702c6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="702c6-124">Header</span><span class="sxs-lookup"><span data-stu-id="702c6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="702c6-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="702c6-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="702c6-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="702c6-126">Library</span></span><br/> | <dl> <span data-ttu-id="702c6-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="702c6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="702c6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="702c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702c6-129">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="702c6-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




