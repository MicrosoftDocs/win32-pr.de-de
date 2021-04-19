---
description: Zeiger auf einen kritischen Abschnitt.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Cbasemediafilter:: m_pLock Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361358"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="53eff-103">Cbasemediafilter:: m \_ Plock-Member</span><span class="sxs-lookup"><span data-stu-id="53eff-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="53eff-104">Zeiger auf einen kritischen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="53eff-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="53eff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53eff-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="53eff-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53eff-106">Remarks</span></span>

<span data-ttu-id="53eff-107">Der kritische Abschnitt wird während der Statusübergänge ([**cbasemediafilter:: Run**](cbasemediafilter-run.md), [**cbasemediafilter::P ause**](cbasemediafilter-pause.md), [**cbasemediafilter:: beenden**](cbasemediafilter-stop.md)), beim Zugriff auf die Referenzuhr ([**cbasemediafilter:: setsyncsource**](cbasemediafilter-setsyncsource.md), [**cbasemediafilter:: getsyncsource**](cbasemediafilter-getsyncsource.md)) und in der [**cbasemediafilter:: IsActive**](cbasemediafilter-isactive.md) -Methode gespeichert.</span><span class="sxs-lookup"><span data-stu-id="53eff-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="53eff-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53eff-108">Requirements</span></span>



| <span data-ttu-id="53eff-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53eff-109">Requirement</span></span> | <span data-ttu-id="53eff-110">Wert</span><span class="sxs-lookup"><span data-stu-id="53eff-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53eff-111">Header</span><span class="sxs-lookup"><span data-stu-id="53eff-111">Header</span></span><br/>  | <dl> <span data-ttu-id="53eff-112"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53eff-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="53eff-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53eff-113">Library</span></span><br/> | <dl> <span data-ttu-id="53eff-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="53eff-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53eff-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53eff-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53eff-116">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="53eff-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




