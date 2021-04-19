---
description: Zeiger auf eine amoviesetup- \_ Filter Struktur.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'Cfactoriytemplate:: m_pAMovieSetup_Filter Member (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370193"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a><span data-ttu-id="994bf-103">Cfactorytemplate:: m \_ pamoviesetup- \_ Filter Element</span><span class="sxs-lookup"><span data-stu-id="994bf-103">CFactoryTemplate::m\_pAMovieSetup\_Filter member</span></span>

<span data-ttu-id="994bf-104">Zeiger auf eine [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="994bf-104">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="994bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="994bf-105">Syntax</span></span>


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a><span data-ttu-id="994bf-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="994bf-106">Remarks</span></span>

<span data-ttu-id="994bf-107">Verwenden Sie diese Struktur, um die Selbstregistrierung eines Filters vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="994bf-107">Use this structure to make a filter self-registering.</span></span> <span data-ttu-id="994bf-108">Wenn es sich bei der Komponente nicht um einen Filter handelt, kann diese Element Variable **null** sein.</span><span class="sxs-lookup"><span data-stu-id="994bf-108">If your component is not a filter, this member variable can be **NULL**.</span></span> <span data-ttu-id="994bf-109">Weitere Informationen finden Sie unter Vorgehensweise beim Registrieren von DirectShow-filtern.</span><span class="sxs-lookup"><span data-stu-id="994bf-109">For more information, see How to Register DirectShow Filters.</span></span>

## <a name="requirements"></a><span data-ttu-id="994bf-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="994bf-110">Requirements</span></span>



| <span data-ttu-id="994bf-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="994bf-111">Requirement</span></span> | <span data-ttu-id="994bf-112">Wert</span><span class="sxs-lookup"><span data-stu-id="994bf-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994bf-113">Header</span><span class="sxs-lookup"><span data-stu-id="994bf-113">Header</span></span><br/>  | <dl> <span data-ttu-id="994bf-114"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="994bf-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="994bf-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="994bf-115">Library</span></span><br/> | <dl> <span data-ttu-id="994bf-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="994bf-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="994bf-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="994bf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994bf-118">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="994bf-118">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




