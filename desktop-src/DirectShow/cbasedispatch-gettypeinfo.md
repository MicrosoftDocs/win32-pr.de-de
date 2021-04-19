---
description: Die GetTypeInfo-Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Cbasedispatch. gettypeingefo-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369694"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="75273-103">Cbasedispatch. gettypeingefo-Methode</span><span class="sxs-lookup"><span data-stu-id="75273-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="75273-104">Die- `GetTypeInfo` Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="75273-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="75273-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75273-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="75273-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75273-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="75273-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="75273-108">Verweis auf einen Schnittstellen Bezeichner (IID), der die-Schnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="75273-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="75273-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="75273-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="75273-110">Typinformationen, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="75273-110">Type information to return.</span></span> <span data-ttu-id="75273-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="75273-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75273-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="75273-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="75273-113">Gebietsschemabezeichner</span><span class="sxs-lookup"><span data-stu-id="75273-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="75273-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="75273-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="75273-115">Adresse einer Variablen, die einen **itypeingefo** -Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="75273-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75273-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75273-116">Return value</span></span>

<span data-ttu-id="75273-117">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="75273-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="75273-118">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="75273-118">Possible values include the following.</span></span>



| <span data-ttu-id="75273-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="75273-119">Return code</span></span>                                                                                             | <span data-ttu-id="75273-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75273-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="75273-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="75273-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="75273-122">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="75273-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="75273-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="75273-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="75273-124">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="75273-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="75273-125"><dt>**Geben Sie \_ E \_ elementnotfound ein.**</dt></span><span class="sxs-lookup"><span data-stu-id="75273-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="75273-126">Der *itinfo* -Parameter ist nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="75273-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75273-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75273-127">Remarks</span></span>

<span data-ttu-id="75273-128">Diese Methode verhält sich wie die **IDispatch:: gettypeingefo** -Methode.</span><span class="sxs-lookup"><span data-stu-id="75273-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="75273-129">Sie enthält jedoch den zusätzlichen Parameter *riid*, der die Schnittstelle angibt, für die Typinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75273-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="75273-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75273-130">Requirements</span></span>



| <span data-ttu-id="75273-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75273-131">Requirement</span></span> | <span data-ttu-id="75273-132">Wert</span><span class="sxs-lookup"><span data-stu-id="75273-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75273-133">Header</span><span class="sxs-lookup"><span data-stu-id="75273-133">Header</span></span><br/>  | <dl> <span data-ttu-id="75273-134"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75273-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75273-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75273-135">Library</span></span><br/> | <dl> <span data-ttu-id="75273-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="75273-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75273-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75273-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75273-138">**Cbasedispatch-Klasse**</span><span class="sxs-lookup"><span data-stu-id="75273-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




