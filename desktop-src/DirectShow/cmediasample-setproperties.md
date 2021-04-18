---
description: 'Die SetProperties-Methode legt die Eigenschaften des Beispiels fest. Diese Methode implementiert die IMediaSample2:: SetProperties-Methode.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Cmediasample. SetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352851"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="84f9c-104">Cmediasample. SetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="84f9c-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="84f9c-105">Die- `SetProperties` Methode legt die Eigenschaften des Beispiels fest.</span><span class="sxs-lookup"><span data-stu-id="84f9c-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="84f9c-106">Diese Methode implementiert die [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) -Methode.</span><span class="sxs-lookup"><span data-stu-id="84f9c-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f9c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="84f9c-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="84f9c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84f9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f9c-109">*cbproperties*</span><span class="sxs-lookup"><span data-stu-id="84f9c-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="84f9c-110">Länge der festzulegenden Eigenschaften Daten (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="84f9c-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="84f9c-111">*pbproperties*</span><span class="sxs-lookup"><span data-stu-id="84f9c-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="84f9c-112">Zeiger auf einen Puffer der Größe *cbproperties*.</span><span class="sxs-lookup"><span data-stu-id="84f9c-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f9c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84f9c-113">Return value</span></span>

<span data-ttu-id="84f9c-114">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="84f9c-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="84f9c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="84f9c-115">Return code</span></span>                                                                                   | <span data-ttu-id="84f9c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84f9c-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="84f9c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="84f9c-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="84f9c-118">Erfolg</span><span class="sxs-lookup"><span data-stu-id="84f9c-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="84f9c-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="84f9c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="84f9c-120">Ungültiges Argument</span><span class="sxs-lookup"><span data-stu-id="84f9c-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="84f9c-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="84f9c-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="84f9c-122">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="84f9c-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="84f9c-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="84f9c-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="84f9c-124">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="84f9c-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="84f9c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84f9c-125">Requirements</span></span>



| <span data-ttu-id="84f9c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84f9c-126">Requirement</span></span> | <span data-ttu-id="84f9c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="84f9c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f9c-128">Header</span><span class="sxs-lookup"><span data-stu-id="84f9c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="84f9c-129"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84f9c-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="84f9c-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84f9c-130">Library</span></span><br/> | <dl> <span data-ttu-id="84f9c-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="84f9c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f9c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84f9c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f9c-133">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="84f9c-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




