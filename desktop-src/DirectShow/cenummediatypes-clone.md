---
description: 'Die Clone-Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die ienummediatypes:: Clone-Methode.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Cenumschlag mediatypes. Clone-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367679"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="28e31-104">Cenum mediatypes. Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="28e31-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="28e31-105">Die- `Clone` Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand.</span><span class="sxs-lookup"><span data-stu-id="28e31-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="28e31-106">Diese Methode implementiert die [**ienummediatypes:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) -Methode.</span><span class="sxs-lookup"><span data-stu-id="28e31-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28e31-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="28e31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28e31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e31-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="28e31-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="28e31-110">Adresse einer Variablen, die einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle des neuen Enumerators empfängt.</span><span class="sxs-lookup"><span data-stu-id="28e31-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e31-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28e31-111">Return value</span></span>

<span data-ttu-id="28e31-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="28e31-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="28e31-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="28e31-113">Return code</span></span>                                                                                                | <span data-ttu-id="28e31-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28e31-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28e31-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28e31-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="28e31-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="28e31-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="28e31-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="28e31-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="28e31-118">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="28e31-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="28e31-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="28e31-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="28e31-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="28e31-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="28e31-121"><dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt></span><span class="sxs-lookup"><span data-stu-id="28e31-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="28e31-122">Der Zustand der PIN wurde geändert und ist nun inkonsistent mit dem Enumerator.</span><span class="sxs-lookup"><span data-stu-id="28e31-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28e31-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28e31-123">Requirements</span></span>



| <span data-ttu-id="28e31-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28e31-124">Requirement</span></span> | <span data-ttu-id="28e31-125">Wert</span><span class="sxs-lookup"><span data-stu-id="28e31-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e31-126">Header</span><span class="sxs-lookup"><span data-stu-id="28e31-126">Header</span></span><br/>  | <dl> <span data-ttu-id="28e31-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28e31-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="28e31-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28e31-128">Library</span></span><br/> | <dl> <span data-ttu-id="28e31-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="28e31-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e31-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28e31-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e31-131">**Cenum mediatypes-Klasse**</span><span class="sxs-lookup"><span data-stu-id="28e31-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




