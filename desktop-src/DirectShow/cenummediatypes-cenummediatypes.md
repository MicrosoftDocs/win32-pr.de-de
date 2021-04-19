---
description: Konstruktormethode.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Cenenmediatypes. cenenmediatypes-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355956"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="006a4-103">Cenenmediatypes. cenenmediatypes-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="006a4-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="006a4-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="006a4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="006a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="006a4-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="006a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="006a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="006a4-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="006a4-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="006a4-108">Ein Zeiger auf die PIN, auf der die Enumeration ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="006a4-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="006a4-109">*Datentypen*</span><span class="sxs-lookup"><span data-stu-id="006a4-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="006a4-110">Ein Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle eines Enumerators, der geklont werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="006a4-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="006a4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="006a4-111">Remarks</span></span>

<span data-ttu-id="006a4-112">Wenn " *pummediatypes* " **null** ist, initialisiert diese Methode den Enumerator bis zum Anfang der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="006a4-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="006a4-113">Andernfalls dupliziert Sie den internen Zustand des Enumerators, der durch " *pummediatypes*" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="006a4-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="006a4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="006a4-114">Requirements</span></span>



| <span data-ttu-id="006a4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="006a4-115">Requirement</span></span> | <span data-ttu-id="006a4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="006a4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="006a4-117">Header</span><span class="sxs-lookup"><span data-stu-id="006a4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="006a4-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="006a4-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="006a4-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="006a4-119">Library</span></span><br/> | <dl> <span data-ttu-id="006a4-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="006a4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="006a4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="006a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006a4-122">**Cenum mediatypes-Klasse**</span><span class="sxs-lookup"><span data-stu-id="006a4-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




