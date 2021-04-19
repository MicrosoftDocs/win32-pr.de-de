---
description: Die Init-Methode initialisiert den streamingindthread.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: CSourceStream.Init-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366773"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="7da7c-103">CSourceStream.Init-Methode</span><span class="sxs-lookup"><span data-stu-id="7da7c-103">CSourceStream.Init method</span></span>

<span data-ttu-id="7da7c-104">Die- `Init` Methode initialisiert den streamingindthread.</span><span class="sxs-lookup"><span data-stu-id="7da7c-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da7c-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="7da7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7da7c-106">Parameters</span></span>

<span data-ttu-id="7da7c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7da7c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7da7c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7da7c-108">Return value</span></span>

<span data-ttu-id="7da7c-109">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7da7c-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7da7c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7da7c-110">Remarks</span></span>

<span data-ttu-id="7da7c-111">Diese Methode muss die erste Thread Anforderung sein, die an die [**csourcestream:: ThreadProc**](csourcestream-threadproc.md) -Methode gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7da7c-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="7da7c-112">Die [**csourcestream:: Active**](csourcestream-active.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7da7c-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da7c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7da7c-113">Requirements</span></span>



| <span data-ttu-id="7da7c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7da7c-114">Requirement</span></span> | <span data-ttu-id="7da7c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7da7c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da7c-116">Header</span><span class="sxs-lookup"><span data-stu-id="7da7c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7da7c-117"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7da7c-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7da7c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7da7c-118">Library</span></span><br/> | <dl> <span data-ttu-id="7da7c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7da7c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da7c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7da7c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da7c-121">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7da7c-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




