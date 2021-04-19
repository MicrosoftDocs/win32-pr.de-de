---
description: Die beginflush-Methode startet einen Löschvorgang.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Cbaserderderer. beginflush-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373823"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="f1be4-103">Cbaserderderer. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="f1be4-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="f1be4-104">Die- `BeginFlush` Methode startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="f1be4-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1be4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1be4-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="f1be4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1be4-106">Parameters</span></span>

<span data-ttu-id="f1be4-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f1be4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1be4-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1be4-108">Return value</span></span>

<span data-ttu-id="f1be4-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f1be4-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1be4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1be4-110">Remarks</span></span>

<span data-ttu-id="f1be4-111">Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie einen Aufruf an die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode empfängt.</span><span class="sxs-lookup"><span data-stu-id="f1be4-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="f1be4-112">Der Filter gibt den streamingingthread frei und gibt jedes Beispiel frei, das für das Rendering gehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="f1be4-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1be4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1be4-113">Requirements</span></span>



| <span data-ttu-id="f1be4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1be4-114">Requirement</span></span> | <span data-ttu-id="f1be4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f1be4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1be4-116">Header</span><span class="sxs-lookup"><span data-stu-id="f1be4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f1be4-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1be4-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f1be4-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1be4-118">Library</span></span><br/> | <dl> <span data-ttu-id="f1be4-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f1be4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1be4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1be4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1be4-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f1be4-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




