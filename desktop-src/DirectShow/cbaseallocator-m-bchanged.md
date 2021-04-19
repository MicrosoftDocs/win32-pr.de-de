---
description: Flag zum angeben, ob sich die Puffer Anforderungen geändert haben.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Cbasezucator:: m_bChanged Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365595"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="2eb2c-103">Cbasezucator:: m- \_ bchanged-Member</span><span class="sxs-lookup"><span data-stu-id="2eb2c-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="2eb2c-104">Flag zum angeben, ob sich die Puffer Anforderungen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="2eb2c-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="2eb2c-105">Die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode legt den Wert auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="2eb2c-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="2eb2c-106">In einer abgeleiteten Klasse sollte die rein virtuelle Methode [**cbasezucator:: zuordc**](cbaseallocator-alloc.md) den Wert auf **false** zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="2eb2c-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="2eb2c-107">Nachdem Puffer zugeordnet wurden, müssen Sie Sie nicht erneut zuordnen, während *m \_ bchanged* den Wert **false** hat.</span><span class="sxs-lookup"><span data-stu-id="2eb2c-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb2c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eb2c-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="2eb2c-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2eb2c-109">Requirements</span></span>



| <span data-ttu-id="2eb2c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2eb2c-110">Requirement</span></span> | <span data-ttu-id="2eb2c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="2eb2c-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb2c-112">Header</span><span class="sxs-lookup"><span data-stu-id="2eb2c-112">Header</span></span><br/>  | <dl> <span data-ttu-id="2eb2c-113"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2eb2c-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2eb2c-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2eb2c-114">Library</span></span><br/> | <dl> <span data-ttu-id="2eb2c-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2eb2c-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb2c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2eb2c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb2c-117">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2eb2c-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




