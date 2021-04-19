---
description: Die Run-Methode signalisiert, dass der streamingthread ausgeführt werden soll.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Csourcestream. Run-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361687"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="1c2a1-103">Csourcestream. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="1c2a1-103">CSourceStream.Run method</span></span>

<span data-ttu-id="1c2a1-104">Die- `Run` Methode signalisiert dem streamingthread, ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1c2a1-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c2a1-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="1c2a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c2a1-106">Parameters</span></span>

<span data-ttu-id="1c2a1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1c2a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c2a1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c2a1-108">Return value</span></span>

<span data-ttu-id="1c2a1-109">Gibt \_ OK oder E \_ unerwartet zurück.</span><span class="sxs-lookup"><span data-stu-id="1c2a1-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c2a1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c2a1-110">Remarks</span></span>

<span data-ttu-id="1c2a1-111">In der Basisklasse hat diese Methode dieselbe Wirkung wie die [**csourcestream::P ause**](csourcestream-pause.md) -Anforderung und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c2a1-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2a1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c2a1-112">Requirements</span></span>



| <span data-ttu-id="1c2a1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c2a1-113">Requirement</span></span> | <span data-ttu-id="1c2a1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1c2a1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2a1-115">Header</span><span class="sxs-lookup"><span data-stu-id="1c2a1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1c2a1-116"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a1-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1c2a1-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c2a1-117">Library</span></span><br/> | <dl> <span data-ttu-id="1c2a1-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c2a1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c2a1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2a1-120">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1c2a1-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




