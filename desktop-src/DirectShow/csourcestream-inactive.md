---
description: 'Die inaktive Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist. Diese Methode überschreibt die cbasepin:: inaktive-Methode. Wenn der streamingingthread aktiv ist, beendet diese Methode ihn und wartet, bis der Thread beendet wird.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Csourcestream. inaktive-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364717"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="46f44-105">Csourcestream. inaktive-Methode</span><span class="sxs-lookup"><span data-stu-id="46f44-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="46f44-106">Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="46f44-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="46f44-107">Diese Methode überschreibt die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="46f44-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="46f44-108">Wenn der streamingingthread aktiv ist, beendet diese Methode ihn und wartet, bis der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="46f44-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f44-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f44-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="46f44-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46f44-110">Parameters</span></span>

<span data-ttu-id="46f44-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="46f44-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46f44-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46f44-112">Return value</span></span>

<span data-ttu-id="46f44-113">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="46f44-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="46f44-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46f44-114">Requirements</span></span>



| <span data-ttu-id="46f44-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46f44-115">Requirement</span></span> | <span data-ttu-id="46f44-116">Wert</span><span class="sxs-lookup"><span data-stu-id="46f44-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f44-117">Header</span><span class="sxs-lookup"><span data-stu-id="46f44-117">Header</span></span><br/>  | <dl> <span data-ttu-id="46f44-118"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46f44-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="46f44-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46f44-119">Library</span></span><br/> | <dl> <span data-ttu-id="46f44-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="46f44-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f44-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46f44-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f44-122">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46f44-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




