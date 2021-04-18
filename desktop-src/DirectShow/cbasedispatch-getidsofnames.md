---
description: Die GetIDsOfNames-Methode ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Cbasedispatch. GetIDsOfNames-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368301"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="dafb1-103">Cbasedispatch. GetIDsOfNames-Methode</span><span class="sxs-lookup"><span data-stu-id="dafb1-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="dafb1-104">Die-Methode ordnet einem `GetIDsOfNames` entsprechenden Satz von DISPIDs einen Satz von Namen zu.</span><span class="sxs-lookup"><span data-stu-id="dafb1-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="dafb1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dafb1-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="dafb1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dafb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dafb1-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="dafb1-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="dafb1-108">Verweis auf einen Schnittstellen Bezeichner (IID), der die-Schnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="dafb1-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="dafb1-109">*rgsznames*</span><span class="sxs-lookup"><span data-stu-id="dafb1-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="dafb1-110">Adresse eines Arrays von breit Zeichen-Zeichen folgen, die die Namen enthalten, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dafb1-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="dafb1-111">*CNAMES*</span><span class="sxs-lookup"><span data-stu-id="dafb1-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="dafb1-112">Größe des Arrays, das vom *rgsznames* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dafb1-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dafb1-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="dafb1-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="dafb1-114">Der Gebiets Schema Kontext, in dem die Namen interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dafb1-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="dafb1-115">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="dafb1-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dafb1-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="dafb1-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="dafb1-117">Zeiger auf ein Array, das die DISPIDs empfängt.</span><span class="sxs-lookup"><span data-stu-id="dafb1-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="dafb1-118">Jedes Element von empfängt einen Bezeichner, der einem der im *rgsznames* -Parameter übergebenen Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="dafb1-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dafb1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dafb1-119">Return value</span></span>

<span data-ttu-id="dafb1-120">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dafb1-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dafb1-121">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="dafb1-121">Possible values include the following.</span></span>



| <span data-ttu-id="dafb1-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dafb1-122">Return code</span></span>                                                                                         | <span data-ttu-id="dafb1-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dafb1-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="dafb1-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dafb1-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="dafb1-125">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="dafb1-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="dafb1-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dafb1-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="dafb1-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="dafb1-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="dafb1-128"><dt>**DISP \_ E \_ unknownname**</dt></span><span class="sxs-lookup"><span data-stu-id="dafb1-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="dafb1-129">Mindestens ein Name ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="dafb1-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dafb1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dafb1-130">Remarks</span></span>

<span data-ttu-id="dafb1-131">Diese Methode verhält sich wie die **IDispatch:: GetIDsOfNames** -Methode, aber der *riid* -Parameter gibt die Schnittstelle an, auf der DispIds abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dafb1-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="dafb1-132">(In der **IDispatch** -Version ist der *riid* -Parameter reserviert.)</span><span class="sxs-lookup"><span data-stu-id="dafb1-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="dafb1-133">Wenn die Methode DISP \_ E \_ unknownname zurückgibt, enthalten die zurückgegebenen DispIds DISPID \_ Unknown für jeden Eintrag, der einem unbekannten Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="dafb1-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="dafb1-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dafb1-134">Requirements</span></span>



| <span data-ttu-id="dafb1-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dafb1-135">Requirement</span></span> | <span data-ttu-id="dafb1-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dafb1-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dafb1-137">Header</span><span class="sxs-lookup"><span data-stu-id="dafb1-137">Header</span></span><br/>  | <dl> <span data-ttu-id="dafb1-138"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dafb1-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dafb1-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dafb1-139">Library</span></span><br/> | <dl> <span data-ttu-id="dafb1-140">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dafb1-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dafb1-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dafb1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dafb1-142">**Cbasedispatch-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dafb1-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




