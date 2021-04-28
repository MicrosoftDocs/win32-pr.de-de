---
description: 'CSourceStream.~CSourceStream-Destruktor : Destruktormethode.'
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: CSourceStream.~CSourceStream-Destruktor (Source.h)
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
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085208"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="c6426-103">CSourceStream.~CSourceStream-Destruktor</span><span class="sxs-lookup"><span data-stu-id="c6426-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="c6426-104">Destruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c6426-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6426-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6426-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="c6426-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6426-106">Remarks</span></span>

<span data-ttu-id="c6426-107">Der Destruktor entfernt den Pin automatisch aus dem besitzenden Filter, indem er [**CSource::RemovePin aufruft.**](csource-removepin.md)</span><span class="sxs-lookup"><span data-stu-id="c6426-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6426-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6426-108">Requirements</span></span>



| <span data-ttu-id="c6426-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6426-109">Requirement</span></span> | <span data-ttu-id="c6426-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c6426-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6426-111">Header</span><span class="sxs-lookup"><span data-stu-id="c6426-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c6426-112"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6426-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c6426-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6426-113">Library</span></span><br/> | <dl> <span data-ttu-id="c6426-114"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c6426-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6426-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6426-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6426-116">**CSourceStream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c6426-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




