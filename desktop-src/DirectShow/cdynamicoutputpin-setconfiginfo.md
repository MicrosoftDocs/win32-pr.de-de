---
description: Die setconfiginfo-Methode gibt den igraphconfig-Zeiger und das-Ereignis zum Abbrechen an.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Cdynamicoutputpin. setconfiginfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368409"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="83483-103">Cdynamicoutputpin. setconfiginfo-Methode</span><span class="sxs-lookup"><span data-stu-id="83483-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="83483-104">Die `SetConfigInfo` -Methode gibt den [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) -Zeiger und das-Ereignis zum Abbrechen an.</span><span class="sxs-lookup"><span data-stu-id="83483-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="83483-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83483-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="83483-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83483-107">*pgraphconfig*</span><span class="sxs-lookup"><span data-stu-id="83483-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="83483-108">Ein Zeiger auf die [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) -Schnittstelle oder **null**.</span><span class="sxs-lookup"><span data-stu-id="83483-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="83483-109">*hstopevent*</span><span class="sxs-lookup"><span data-stu-id="83483-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="83483-110">Handle für ein Ereignis, das signalisiert wird, wenn der Filter beendet wird, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="83483-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83483-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83483-111">Return value</span></span>

<span data-ttu-id="83483-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="83483-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83483-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83483-113">Remarks</span></span>

<span data-ttu-id="83483-114">Der Filter muss diese Methode aufzurufen, wenn er dem Filter Diagramm Beitritt.</span><span class="sxs-lookup"><span data-stu-id="83483-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="83483-115">Der Filter Graph-Manager unterstützt **igraphconfig**.</span><span class="sxs-lookup"><span data-stu-id="83483-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="83483-116">Erstellen Sie für den *hstopevent* -Parameter ein manuelles Zurücksetzungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="83483-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="83483-117">Wenn der Filter das Filter Diagramm verlässt, muss diese Methode erneut mit **null** für beide Parameter aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83483-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="83483-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83483-118">Requirements</span></span>



| <span data-ttu-id="83483-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83483-119">Requirement</span></span> | <span data-ttu-id="83483-120">Wert</span><span class="sxs-lookup"><span data-stu-id="83483-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83483-121">Header</span><span class="sxs-lookup"><span data-stu-id="83483-121">Header</span></span><br/>  | <dl> <span data-ttu-id="83483-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83483-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="83483-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83483-123">Library</span></span><br/> | <dl> <span data-ttu-id="83483-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="83483-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83483-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83483-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83483-126">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="83483-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




