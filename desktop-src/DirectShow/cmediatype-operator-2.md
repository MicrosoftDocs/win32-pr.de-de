---
description: Dieser Operator überlädt den Zuweisungs Operator zum Kopieren eines Medientyps.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Cmediatype. cmediatype:: Operator =-Methode (mtype. h)-mtype-Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389036"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="b3457-103">Cmediatype. cmediatype:: Operator =-Methode (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="b3457-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="b3457-104">Dieser Operator überlädt den Zuweisungs Operator zum Kopieren eines Medientyps.</span><span class="sxs-lookup"><span data-stu-id="b3457-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3457-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3457-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="b3457-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3457-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3457-107">*mtype* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="b3457-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b3457-108">Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3457-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3457-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3457-109">Return value</span></span>

<span data-ttu-id="b3457-110">Gibt einen Verweis auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b3457-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3457-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3457-111">Requirements</span></span>



| <span data-ttu-id="b3457-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3457-112">Requirement</span></span> | <span data-ttu-id="b3457-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b3457-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3457-114">Header</span><span class="sxs-lookup"><span data-stu-id="b3457-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b3457-115"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3457-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b3457-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3457-116">Library</span></span><br/> | <dl> <span data-ttu-id="b3457-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b3457-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3457-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3457-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3457-119">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b3457-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




