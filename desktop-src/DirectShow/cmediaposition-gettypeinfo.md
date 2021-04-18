---
description: Die GetTypeInfo-Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Cmediaposition. GetTypeInfo-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361014"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="17946-103">Cmediaposition. GetTypeInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="17946-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="17946-104">Die- `GetTypeInfo` Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="17946-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="17946-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17946-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="17946-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17946-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17946-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="17946-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="17946-108">Typinformationen, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17946-108">Type information to return.</span></span> <span data-ttu-id="17946-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="17946-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="17946-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="17946-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="17946-111">Gebietsschemabezeichner</span><span class="sxs-lookup"><span data-stu-id="17946-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="17946-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="17946-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="17946-113">Adresse einer Variablen, die einen **itypeingefo** -Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="17946-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17946-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17946-114">Return value</span></span>

<span data-ttu-id="17946-115">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17946-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="17946-116">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="17946-116">Possible values include the following.</span></span>



| <span data-ttu-id="17946-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="17946-117">Return code</span></span>                                                                                             | <span data-ttu-id="17946-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17946-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="17946-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17946-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="17946-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="17946-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="17946-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="17946-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="17946-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="17946-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="17946-123"><dt>**Geben Sie \_ E \_ elementnotfound ein.**</dt></span><span class="sxs-lookup"><span data-stu-id="17946-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="17946-124">Der *itinfo* -Parameter ist nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="17946-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17946-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17946-125">Requirements</span></span>



| <span data-ttu-id="17946-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17946-126">Requirement</span></span> | <span data-ttu-id="17946-127">Wert</span><span class="sxs-lookup"><span data-stu-id="17946-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17946-128">Header</span><span class="sxs-lookup"><span data-stu-id="17946-128">Header</span></span><br/>  | <dl> <span data-ttu-id="17946-129"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17946-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17946-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17946-130">Library</span></span><br/> | <dl> <span data-ttu-id="17946-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="17946-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17946-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17946-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17946-133">**Cmediaposition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="17946-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




