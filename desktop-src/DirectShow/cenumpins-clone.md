---
description: 'Die Clone-Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die iumumpins:: Clone-Methode.'
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Cenumpins. Clone-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372137"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="1a8d5-104">Cenumpins. Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="1a8d5-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="1a8d5-105">Die- `Clone` Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="1a8d5-106">Diese Methode implementiert die [**iumumpins:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a8d5-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1a8d5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a8d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a8d5-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="1a8d5-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="1a8d5-110">Adresse einer Variablen, die einen Zeiger auf die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle des neuen Enumerators empfängt.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a8d5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a8d5-111">Return value</span></span>

<span data-ttu-id="1a8d5-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1a8d5-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1a8d5-113">Return code</span></span>                                                                                                | <span data-ttu-id="1a8d5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a8d5-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a8d5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d5-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1a8d5-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="1a8d5-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="1a8d5-118">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1a8d5-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d5-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="1a8d5-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="1a8d5-121"><dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d5-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="1a8d5-122">Der Zustand des Filters wurde geändert und ist nun inkonsistent mit dem Enumerator.</span><span class="sxs-lookup"><span data-stu-id="1a8d5-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a8d5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a8d5-123">Requirements</span></span>



| <span data-ttu-id="1a8d5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a8d5-124">Requirement</span></span> | <span data-ttu-id="1a8d5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1a8d5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8d5-126">Header</span><span class="sxs-lookup"><span data-stu-id="1a8d5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1a8d5-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d5-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a8d5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a8d5-128">Library</span></span><br/> | <dl> <span data-ttu-id="1a8d5-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8d5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a8d5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a8d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8d5-131">**Cenumpins-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1a8d5-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




