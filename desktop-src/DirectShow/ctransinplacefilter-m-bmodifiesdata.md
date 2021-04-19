---
description: Die m \_ bmodifiesdata-Member-Variable gibt an, ob der Filter die Beispiel Daten ändert, die empfangen werden. Der Wert wird im ctransinplacefilter-Konstruktor festgelegt, jedoch ist der Standardwert true.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Ctransinplacefilter:: m_bModifiesData Member (transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361920"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="f18d5-104">Ctransinplacefilter:: m \_ bmodifiesdata-Member</span><span class="sxs-lookup"><span data-stu-id="f18d5-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="f18d5-105">Die `m_bModifiesData` Member-Variable gibt an, ob der Filter die Beispiel Daten ändert, die empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="f18d5-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="f18d5-106">Der Wert wird im **ctransinplacefilter** -Konstruktor festgelegt, jedoch ist der Standardwert **true**.</span><span class="sxs-lookup"><span data-stu-id="f18d5-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f18d5-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="f18d5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f18d5-108">Remarks</span></span>

<span data-ttu-id="f18d5-109">Diese Variable wirkt sich darauf aus, wie der Filter die Zuweisung aushandtert.</span><span class="sxs-lookup"><span data-stu-id="f18d5-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="f18d5-110">Wenn der Wert **true** ist, kann der Filter keine schreibgeschützte Zuweisung für beide Pin-Verbindungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f18d5-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="f18d5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f18d5-111">Requirements</span></span>



| <span data-ttu-id="f18d5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f18d5-112">Requirement</span></span> | <span data-ttu-id="f18d5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f18d5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18d5-114">Header</span><span class="sxs-lookup"><span data-stu-id="f18d5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f18d5-115"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f18d5-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f18d5-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f18d5-116">Library</span></span><br/> | <dl> <span data-ttu-id="f18d5-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f18d5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18d5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f18d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18d5-119">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f18d5-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




