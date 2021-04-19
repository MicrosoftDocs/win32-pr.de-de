---
description: Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Cbasepin:: m_bRunTimeError Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370825"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="4ea6b-103">Cbasepin:: m- \_ Member von bruntimeerror</span><span class="sxs-lookup"><span data-stu-id="4ea6b-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="4ea6b-104">Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ea6b-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="4ea6b-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ea6b-106">Remarks</span></span>

<span data-ttu-id="4ea6b-107">Dieses Flag ist standardmäßig auf **false** eingestellt.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="4ea6b-108">Legen Sie das-Flag auf **true** fest, wenn beim Streaming ein Laufzeitfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="4ea6b-109">Die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode setzt das Flag auf **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea6b-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea6b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ea6b-110">Requirements</span></span>



| <span data-ttu-id="4ea6b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ea6b-111">Requirement</span></span> | <span data-ttu-id="4ea6b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4ea6b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea6b-113">Header</span><span class="sxs-lookup"><span data-stu-id="4ea6b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4ea6b-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ea6b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ea6b-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ea6b-115">Library</span></span><br/> | <dl> <span data-ttu-id="4ea6b-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4ea6b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea6b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ea6b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea6b-118">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4ea6b-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




