---
description: 'CBaseDispatch.GetIDsOfNames-Methode: Die GetIDsOfNames-Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.'
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: CBaseDispatch.GetIDsOfNames-Methode (Ctlutil.h)
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
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099918"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="b2375-103">CBaseDispatch.GetIDsOfNames-Methode</span><span class="sxs-lookup"><span data-stu-id="b2375-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="b2375-104">Die `GetIDsOfNames` -Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.</span><span class="sxs-lookup"><span data-stu-id="b2375-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2375-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2375-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="b2375-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2375-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2375-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="b2375-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="b2375-108">Verweis auf einen Schnittstellenbezeichner (IID), der die Schnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="b2375-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b2375-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="b2375-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="b2375-110">Adresse eines Arrays von Breitzeichenzeichenfolgen, die die namen enthalten, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2375-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="b2375-111">*cNames*</span><span class="sxs-lookup"><span data-stu-id="b2375-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="b2375-112">Die Größe des Arrays, das durch den *rgszNames-Parameter angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="b2375-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2375-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="b2375-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b2375-114">Der Kontext des Orts, in dem die Namen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b2375-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="b2375-115">Kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="b2375-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2375-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="b2375-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="b2375-117">Zeiger auf ein Array, das die DISPIDs empfängt.</span><span class="sxs-lookup"><span data-stu-id="b2375-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="b2375-118">Jedes Element von empfängt einen Bezeichner, der einem der im *rgszNames-Parameter* übergebenen Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b2375-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2375-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2375-119">Return value</span></span>

<span data-ttu-id="b2375-120">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2375-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b2375-121">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="b2375-121">Possible values include the following.</span></span>



| <span data-ttu-id="b2375-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b2375-122">Return code</span></span>                                                                                         | <span data-ttu-id="b2375-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2375-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="b2375-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2375-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="b2375-125">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b2375-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b2375-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b2375-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="b2375-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b2375-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="b2375-128"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="b2375-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="b2375-129">Mindestens einer der Namen war nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="b2375-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2375-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2375-130">Remarks</span></span>

<span data-ttu-id="b2375-131">Diese Methode verhält sich wie die **IDispatch::GetIDsOfNames-Methode,** aber der *riid-Parameter* gibt die Schnittstelle an, über die DISPIDs abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2375-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="b2375-132">(In der **IDispatch-Version** ist der *riid-Parameter* reserviert.)</span><span class="sxs-lookup"><span data-stu-id="b2375-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="b2375-133">Wenn die Methode DISP \_ E \_ UNKNOWNNAME zurückgibt, enthalten die zurückgegebenen DISPIDs DISPID UNKNOWN für jeden Eintrag, der \_ einem unbekannten Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b2375-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2375-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2375-134">Requirements</span></span>



| <span data-ttu-id="b2375-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2375-135">Requirement</span></span> | <span data-ttu-id="b2375-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b2375-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2375-137">Header</span><span class="sxs-lookup"><span data-stu-id="b2375-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b2375-138"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2375-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2375-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2375-139">Library</span></span><br/> | <dl> <span data-ttu-id="b2375-140"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b2375-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2375-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2375-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2375-142">**CBaseDispatch-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b2375-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




