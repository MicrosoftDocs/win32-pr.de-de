---
description: Anzahl der Puffer, die bereitgestellt werden sollen.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Cbasezucator:: m_lCount Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372139"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="7872c-103">Cbasezucator:: m \_ lCount-Member</span><span class="sxs-lookup"><span data-stu-id="7872c-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="7872c-104">Anzahl der Puffer, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7872c-104">Number of buffers to provide.</span></span> <span data-ttu-id="7872c-105">Die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="7872c-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="7872c-106">Die Puffer werden erst zugeordnet, wenn die [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7872c-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="7872c-107">Die aktuelle Anzahl der zugeordneten Puffer wird von der Variablen [**cbasezucator:: m \_ lzugeordnete**](cbaseallocator-m-lallocated.md) Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="7872c-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7872c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7872c-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="7872c-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7872c-109">Requirements</span></span>



| <span data-ttu-id="7872c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7872c-110">Requirement</span></span> | <span data-ttu-id="7872c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="7872c-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7872c-112">Header</span><span class="sxs-lookup"><span data-stu-id="7872c-112">Header</span></span><br/>  | <dl> <span data-ttu-id="7872c-113"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7872c-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7872c-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7872c-114">Library</span></span><br/> | <dl> <span data-ttu-id="7872c-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7872c-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7872c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7872c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7872c-117">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7872c-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




