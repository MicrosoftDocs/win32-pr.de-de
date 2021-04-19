---
description: Die addpin-Methode fügt dem Filter eine neue Ausgabe-PIN hinzu.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: CSource. addpin-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352833"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="3073b-103">CSource. addpin-Methode</span><span class="sxs-lookup"><span data-stu-id="3073b-103">CSource.AddPin method</span></span>

<span data-ttu-id="3073b-104">Die- `AddPin` Methode fügt dem Filter eine neue Ausgabe-PIN hinzu.</span><span class="sxs-lookup"><span data-stu-id="3073b-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3073b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3073b-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="3073b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3073b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3073b-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="3073b-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="3073b-108">Zeiger auf das [**csourcestream**](csourcestream.md) -Objekt, das die PIN implementiert.</span><span class="sxs-lookup"><span data-stu-id="3073b-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3073b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3073b-109">Return value</span></span>

<span data-ttu-id="3073b-110">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3073b-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3073b-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3073b-111">Return code</span></span>                                                                                   | <span data-ttu-id="3073b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3073b-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="3073b-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3073b-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3073b-114">Erfolg</span><span class="sxs-lookup"><span data-stu-id="3073b-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="3073b-115"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3073b-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3073b-116">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="3073b-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3073b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3073b-117">Remarks</span></span>

<span data-ttu-id="3073b-118">Wenn Sie eine neue PIN erstellen, die von **csourcestream** abgeleitet ist, ruft der **csourcestream** -Konstruktor diese Methode automatisch auf, um dem Filter die Ausgabe-PIN hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3073b-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3073b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3073b-119">Requirements</span></span>



| <span data-ttu-id="3073b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3073b-120">Requirement</span></span> | <span data-ttu-id="3073b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3073b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3073b-122">Header</span><span class="sxs-lookup"><span data-stu-id="3073b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3073b-123"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3073b-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3073b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3073b-124">Library</span></span><br/> | <dl> <span data-ttu-id="3073b-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3073b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3073b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3073b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3073b-127">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3073b-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




