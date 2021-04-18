---
description: Dekonstruktormethode.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Csourcestream. ~ csourcestream-debugtor (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372106"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="60d77-103">Csourcestream. ~ csourcestream-Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="60d77-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="60d77-104">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="60d77-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60d77-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="60d77-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60d77-106">Remarks</span></span>

<span data-ttu-id="60d77-107">Der Dekonstruktor entfernt die PIN automatisch aus dem besitzenden Filter, indem [**CSource:: removepin**](csource-removepin.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="60d77-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60d77-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60d77-108">Requirements</span></span>



| <span data-ttu-id="60d77-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60d77-109">Requirement</span></span> | <span data-ttu-id="60d77-110">Wert</span><span class="sxs-lookup"><span data-stu-id="60d77-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d77-111">Header</span><span class="sxs-lookup"><span data-stu-id="60d77-111">Header</span></span><br/>  | <dl> <span data-ttu-id="60d77-112"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60d77-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="60d77-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60d77-113">Library</span></span><br/> | <dl> <span data-ttu-id="60d77-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="60d77-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d77-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60d77-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d77-116">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="60d77-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




