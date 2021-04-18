---
description: Die matchespartial-Methode bestimmt, ob dieser Medientyp mit einem teilweise angegebenen Medientyp übereinstimmt.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Cmediatype. matchespartial-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372632"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="4cffa-103">Cmediatype. matchespartial-Methode</span><span class="sxs-lookup"><span data-stu-id="4cffa-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="4cffa-104">Die- `MatchesPartial` Methode bestimmt, ob dieser Medientyp mit einem teilweise angegebenen Medientyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4cffa-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cffa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cffa-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="4cffa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cffa-107">*ppartiell*</span><span class="sxs-lookup"><span data-stu-id="4cffa-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="4cffa-108">Zeiger auf den Medientyp, der abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cffa-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cffa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cffa-109">Return value</span></span>

<span data-ttu-id="4cffa-110">Gibt **true** zurück, wenn die Medientypen Stimmen.</span><span class="sxs-lookup"><span data-stu-id="4cffa-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="4cffa-111">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4cffa-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cffa-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cffa-112">Remarks</span></span>

<span data-ttu-id="4cffa-113">Der von *ppartial* angegebene Medientyp kann den Wert GUID \_ NULL für den Haupttyp, den Untertyp oder den Formattyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4cffa-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="4cffa-114">Alle Elemente mit GUID- \_ NULL-Werten werden nicht getestet.</span><span class="sxs-lookup"><span data-stu-id="4cffa-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="4cffa-115">(In der Tat GUID \_ Null fungiert als Platzhalter.) Member mit anderen Werten als GUID \_ null müssen mit dem Medientyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="4cffa-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cffa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cffa-116">Requirements</span></span>



| <span data-ttu-id="4cffa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cffa-117">Requirement</span></span> | <span data-ttu-id="4cffa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4cffa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cffa-119">Header</span><span class="sxs-lookup"><span data-stu-id="4cffa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4cffa-120"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cffa-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4cffa-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cffa-121">Library</span></span><br/> | <dl> <span data-ttu-id="4cffa-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4cffa-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cffa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cffa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cffa-124">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4cffa-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




