---
description: CEnumMediaTypes.CEnumMediaTypes-Konstruktor – Konstruktormethode.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: CEnumMediaTypes.CEnumMediaTypes-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095678"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="3854f-103">CEnumMediaTypes.CEnumMediaTypes-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3854f-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="3854f-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="3854f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3854f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3854f-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="3854f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3854f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3854f-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="3854f-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="3854f-108">Zeiger auf den Stecknadel, an dem die Enumeration ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3854f-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="3854f-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="3854f-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="3854f-110">Zeiger auf die [**IEnumMediaTypes-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) eines zu klonenden Enumerators oder **NULL.**</span><span class="sxs-lookup"><span data-stu-id="3854f-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3854f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3854f-111">Remarks</span></span>

<span data-ttu-id="3854f-112">Wenn *pEnumMediaTypes* **NULL** ist, initialisiert diese Methode den Enumerator am Anfang der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="3854f-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="3854f-113">Andernfalls wird der interne Zustand des durch *pEnumMediaTypes* angegebenen Enumerators dupliziert.</span><span class="sxs-lookup"><span data-stu-id="3854f-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3854f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3854f-114">Requirements</span></span>



| <span data-ttu-id="3854f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3854f-115">Requirement</span></span> | <span data-ttu-id="3854f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3854f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3854f-117">Header</span><span class="sxs-lookup"><span data-stu-id="3854f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3854f-118"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3854f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3854f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3854f-119">Library</span></span><br/> | <dl> <span data-ttu-id="3854f-120"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3854f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3854f-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3854f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3854f-122">**CEnumMediaTypes-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3854f-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




