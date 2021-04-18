---
description: Blockierender Zustand.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Cdynamicoutputpin:: m_BlockState Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361055"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="6bd31-103">Cdynamicoutputpin:: m \_ blockstate-Member</span><span class="sxs-lookup"><span data-stu-id="6bd31-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="6bd31-104">Blockierender Zustand.</span><span class="sxs-lookup"><span data-stu-id="6bd31-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bd31-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="6bd31-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bd31-106">Remarks</span></span>

<span data-ttu-id="6bd31-107">Die folgenden Zustände sind definiert:</span><span class="sxs-lookup"><span data-stu-id="6bd31-107">The following states are defined:</span></span>

-   <span data-ttu-id="6bd31-108">nicht \_ blockiert</span><span class="sxs-lookup"><span data-stu-id="6bd31-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="6bd31-109">PENDING (AUSSTEHEND)</span><span class="sxs-lookup"><span data-stu-id="6bd31-109">PENDING</span></span>
-   <span data-ttu-id="6bd31-110">Ge</span><span class="sxs-lookup"><span data-stu-id="6bd31-110">BLOCKED</span></span>

<span data-ttu-id="6bd31-111">Bevor Sie auf diese Variable zugreifen, halten Sie den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="6bd31-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd31-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bd31-112">Requirements</span></span>



| <span data-ttu-id="6bd31-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bd31-113">Requirement</span></span> | <span data-ttu-id="6bd31-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6bd31-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd31-115">Header</span><span class="sxs-lookup"><span data-stu-id="6bd31-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6bd31-116"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bd31-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6bd31-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6bd31-117">Library</span></span><br/> | <dl> <span data-ttu-id="6bd31-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6bd31-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd31-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bd31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd31-120">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6bd31-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




