---
description: Mit der removepin-Methode wird eine angegebene PIN aus dem Filter entfernt. Die-Methode löscht die PIN nicht.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: CSource. removepin-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361010"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="0ce4c-104">CSource. removepin-Methode</span><span class="sxs-lookup"><span data-stu-id="0ce4c-104">CSource.RemovePin method</span></span>

<span data-ttu-id="0ce4c-105">Mit der- `RemovePin` Methode wird eine angegebene PIN aus dem Filter entfernt.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="0ce4c-106">Die-Methode löscht die PIN nicht.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce4c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ce4c-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="0ce4c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ce4c-109">*pStream*</span><span class="sxs-lookup"><span data-stu-id="0ce4c-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="0ce4c-110">Zeiger auf das [**csourcestream**](csourcestream.md) -Objekt, das die PIN implementiert.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ce4c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ce4c-111">Return value</span></span>

<span data-ttu-id="0ce4c-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0ce4c-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0ce4c-113">Return code</span></span>                                                                             | <span data-ttu-id="0ce4c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ce4c-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0ce4c-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ce4c-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0ce4c-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="0ce4c-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0ce4c-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0ce4c-118">Der Filter enthält diese PIN nicht.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ce4c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ce4c-119">Remarks</span></span>

<span data-ttu-id="0ce4c-120">Die dekonstruktormethode ruft diese Methode auf, um die Ausgabe-PIN aus dem Filter zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0ce4c-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce4c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ce4c-121">Requirements</span></span>



| <span data-ttu-id="0ce4c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ce4c-122">Requirement</span></span> | <span data-ttu-id="0ce4c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0ce4c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce4c-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ce4c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0ce4c-125"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ce4c-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0ce4c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ce4c-126">Library</span></span><br/> | <dl> <span data-ttu-id="0ce4c-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0ce4c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce4c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ce4c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce4c-129">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0ce4c-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




