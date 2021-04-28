---
description: 'CMediaPosition.GetIDsOfNames-Methode: Die GetIDsOfNames-Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.'
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: CMediaPosition.GetIDsOfNames-Methode (Ctlutil.h)
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
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095528"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="6895d-103">CMediaPosition.GetIDsOfNames-Methode</span><span class="sxs-lookup"><span data-stu-id="6895d-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="6895d-104">Die `GetIDsOfNames` -Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.</span><span class="sxs-lookup"><span data-stu-id="6895d-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="6895d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6895d-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="6895d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6895d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6895d-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="6895d-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="6895d-108">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6895d-108">Reserved.</span></span> <span data-ttu-id="6895d-109">Verwenden Sie IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="6895d-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="6895d-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="6895d-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="6895d-111">Adresse eines Arrays von Breitzeichenzeichenfolgen, die die namen enthalten, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6895d-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="6895d-112">*cNames*</span><span class="sxs-lookup"><span data-stu-id="6895d-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="6895d-113">Die Größe des Arrays, das durch den *rgszNames-Parameter angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6895d-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6895d-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="6895d-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="6895d-115">Der Kontext des Orts, in dem die Namen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="6895d-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="6895d-116">Kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="6895d-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6895d-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="6895d-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="6895d-118">Zeiger auf ein Array, das die DISPIDs empfängt.</span><span class="sxs-lookup"><span data-stu-id="6895d-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="6895d-119">Jedes Element von empfängt einen Bezeichner, der einem der im *rgszNames-Parameter* übergebenen Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6895d-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6895d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6895d-120">Return value</span></span>

<span data-ttu-id="6895d-121">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="6895d-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6895d-122">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="6895d-122">Possible values include the following.</span></span>



| <span data-ttu-id="6895d-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6895d-123">Return code</span></span>                                                                                         | <span data-ttu-id="6895d-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6895d-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="6895d-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6895d-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="6895d-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6895d-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="6895d-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6895d-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="6895d-128">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6895d-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="6895d-129"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="6895d-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="6895d-130">Mindestens einer der Namen war nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="6895d-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6895d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6895d-131">Requirements</span></span>



| <span data-ttu-id="6895d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6895d-132">Requirement</span></span> | <span data-ttu-id="6895d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6895d-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6895d-134">Header</span><span class="sxs-lookup"><span data-stu-id="6895d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="6895d-135"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6895d-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6895d-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6895d-136">Library</span></span><br/> | <dl> <span data-ttu-id="6895d-137"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6895d-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6895d-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6895d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6895d-139">**CMediaPosition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6895d-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




