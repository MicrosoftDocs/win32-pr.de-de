---
description: Die GetIDsOfNames-Methode ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Cmediaposition. GetIDsOfNames-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369241"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="34f67-103">Cmediaposition. GetIDsOfNames-Methode</span><span class="sxs-lookup"><span data-stu-id="34f67-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="34f67-104">Die-Methode ordnet einem `GetIDsOfNames` entsprechenden Satz von DISPIDs einen Satz von Namen zu.</span><span class="sxs-lookup"><span data-stu-id="34f67-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34f67-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="34f67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34f67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f67-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="34f67-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="34f67-108">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="34f67-108">Reserved.</span></span> <span data-ttu-id="34f67-109">Verwenden Sie IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="34f67-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="34f67-110">*rgsznames*</span><span class="sxs-lookup"><span data-stu-id="34f67-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="34f67-111">Adresse eines Arrays von breit Zeichen-Zeichen folgen, die die Namen enthalten, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34f67-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="34f67-112">*CNAMES*</span><span class="sxs-lookup"><span data-stu-id="34f67-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="34f67-113">Größe des Arrays, das vom *rgsznames* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="34f67-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="34f67-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="34f67-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="34f67-115">Der Gebiets Schema Kontext, in dem die Namen interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34f67-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="34f67-116">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="34f67-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34f67-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="34f67-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="34f67-118">Zeiger auf ein Array, das die DISPIDs empfängt.</span><span class="sxs-lookup"><span data-stu-id="34f67-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="34f67-119">Jedes Element von empfängt einen Bezeichner, der einem der im *rgsznames* -Parameter übergebenen Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="34f67-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f67-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34f67-120">Return value</span></span>

<span data-ttu-id="34f67-121">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="34f67-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="34f67-122">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="34f67-122">Possible values include the following.</span></span>



| <span data-ttu-id="34f67-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="34f67-123">Return code</span></span>                                                                                         | <span data-ttu-id="34f67-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34f67-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="34f67-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34f67-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="34f67-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="34f67-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="34f67-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="34f67-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="34f67-128">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="34f67-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="34f67-129"><dt>**DISP \_ E \_ unknownname**</dt></span><span class="sxs-lookup"><span data-stu-id="34f67-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="34f67-130">Mindestens ein Name ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="34f67-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="34f67-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f67-131">Requirements</span></span>



| <span data-ttu-id="34f67-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34f67-132">Requirement</span></span> | <span data-ttu-id="34f67-133">Wert</span><span class="sxs-lookup"><span data-stu-id="34f67-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f67-134">Header</span><span class="sxs-lookup"><span data-stu-id="34f67-134">Header</span></span><br/>  | <dl> <span data-ttu-id="34f67-135"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34f67-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34f67-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34f67-136">Library</span></span><br/> | <dl> <span data-ttu-id="34f67-137">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="34f67-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f67-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34f67-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f67-139">**Cmediaposition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="34f67-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




