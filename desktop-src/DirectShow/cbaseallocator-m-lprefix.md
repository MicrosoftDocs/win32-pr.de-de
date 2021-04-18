---
description: Präfix jedes Puffers in Bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Cbasezucator:: m_lPrefix Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352884"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="463d6-103">Cbasezucator:: m \_ lprefix-Member</span><span class="sxs-lookup"><span data-stu-id="463d6-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="463d6-104">Präfix jedes Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="463d6-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="463d6-105">Wenn der Wert ungleich 0 (null) ist, wird jedem Puffer Zeiger, der von der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode zurückgegeben wird, ein Block von Bytes der Größe *m \_ lprefix* vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="463d6-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="463d6-106">Dieser Speicherblock wird als *Präfix* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="463d6-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="463d6-107">Die Member-Variable [**cbasezucator:: m \_ LSIZE**](cbaseallocator-m-lsize.md) enthält nicht den Präfix Wert.</span><span class="sxs-lookup"><span data-stu-id="463d6-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="463d6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="463d6-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="463d6-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="463d6-109">Requirements</span></span>



| <span data-ttu-id="463d6-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="463d6-110">Requirement</span></span> | <span data-ttu-id="463d6-111">Wert</span><span class="sxs-lookup"><span data-stu-id="463d6-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463d6-112">Header</span><span class="sxs-lookup"><span data-stu-id="463d6-112">Header</span></span><br/>  | <dl> <span data-ttu-id="463d6-113"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="463d6-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="463d6-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="463d6-114">Library</span></span><br/> | <dl> <span data-ttu-id="463d6-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="463d6-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463d6-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="463d6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463d6-117">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="463d6-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




