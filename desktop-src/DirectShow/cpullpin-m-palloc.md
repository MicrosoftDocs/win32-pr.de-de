---
description: Die \_ Member-Variable m palloc ist ein Zeiger auf die imemzuordcator-Schnittstelle der Speicherzuweisung.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Cpullpin:: m_pAlloc Member (pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359709"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="3c149-103">Cpullpin:: m \_ palloc-Member</span><span class="sxs-lookup"><span data-stu-id="3c149-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="3c149-104">Die `m_pAlloc` Member-Variable ist ein Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle der Speicherzuweisung.</span><span class="sxs-lookup"><span data-stu-id="3c149-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c149-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c149-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="3c149-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c149-106">Remarks</span></span>

<span data-ttu-id="3c149-107">Die [**cpullpin::D ecidezuordcator**](cpullpin-decideallocator.md) -Methode legt diese Element Variable fest.</span><span class="sxs-lookup"><span data-stu-id="3c149-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c149-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c149-108">Requirements</span></span>



| <span data-ttu-id="3c149-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c149-109">Requirement</span></span> | <span data-ttu-id="3c149-110">Wert</span><span class="sxs-lookup"><span data-stu-id="3c149-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c149-111">Header</span><span class="sxs-lookup"><span data-stu-id="3c149-111">Header</span></span><br/>  | <dl> <span data-ttu-id="3c149-112"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c149-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="3c149-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c149-113">Library</span></span><br/> | <dl> <span data-ttu-id="3c149-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3c149-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c149-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c149-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c149-116">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3c149-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




