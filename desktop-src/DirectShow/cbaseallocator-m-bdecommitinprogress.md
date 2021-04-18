---
description: Flag zum angeben, ob ein Decommit-Vorgang ausgeführt wird.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Cbasezucator:: m_bDecommitInProgress Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357597"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="4cffe-103">Cbasezucator:: m \_ bdecommitinprogress-Member</span><span class="sxs-lookup"><span data-stu-id="4cffe-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="4cffe-104">Flag zum angeben, ob ein Decommit-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cffe-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="4cffe-105">Der Wert ist " **true** ", nachdem die Methode " [**cbasezucator::D ecommit**](cbaseallocator-decommit.md) " aufgerufen wurde, aber bevor alle Puffer freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="4cffe-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="4cffe-106">Wenn der Wert **true** lautet, schlägt die [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="4cffe-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="4cffe-107">Außerdem sollte die Zuweisung nicht selbst gelöscht werden, wenn der Wert **true** ist.</span><span class="sxs-lookup"><span data-stu-id="4cffe-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cffe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cffe-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="4cffe-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4cffe-109">Requirements</span></span>



| <span data-ttu-id="4cffe-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cffe-110">Requirement</span></span> | <span data-ttu-id="4cffe-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4cffe-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cffe-112">Header</span><span class="sxs-lookup"><span data-stu-id="4cffe-112">Header</span></span><br/>  | <dl> <span data-ttu-id="4cffe-113"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cffe-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4cffe-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cffe-114">Library</span></span><br/> | <dl> <span data-ttu-id="4cffe-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4cffe-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cffe-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cffe-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cffe-117">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4cffe-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




