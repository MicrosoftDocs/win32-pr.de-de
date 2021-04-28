---
description: 'CMediaPosition.GetTypeInfo-Methode: Die GetTypeInfo-Methode ruft die Typinformationen für das Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen.'
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: CMediaPosition.GetTypeInfo-Methode (Ctlutil.h)
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
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099138"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="c5276-103">CMediaPosition.GetTypeInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="c5276-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="c5276-104">Die `GetTypeInfo` -Methode ruft die Typinformationen für das -Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5276-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5276-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5276-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="c5276-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5276-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5276-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="c5276-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c5276-108">Geben Sie informationen ein, die sie zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5276-108">Type information to return.</span></span> <span data-ttu-id="c5276-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c5276-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5276-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="c5276-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="c5276-111">Gebietsschemabezeichner</span><span class="sxs-lookup"><span data-stu-id="c5276-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c5276-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="c5276-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c5276-113">Adresse einer Variablen, die einen **ITypeInfo-Zeiger** empfängt.</span><span class="sxs-lookup"><span data-stu-id="c5276-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5276-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5276-114">Return value</span></span>

<span data-ttu-id="c5276-115">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="c5276-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c5276-116">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="c5276-116">Possible values include the following.</span></span>



| <span data-ttu-id="c5276-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c5276-117">Return code</span></span>                                                                                             | <span data-ttu-id="c5276-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5276-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c5276-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5276-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c5276-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c5276-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="c5276-121"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="c5276-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="c5276-122"> NULL-Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="c5276-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="c5276-123"><dt>**TYP \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="c5276-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="c5276-124">Der *itinfo-Parameter* ist nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c5276-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c5276-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5276-125">Requirements</span></span>



| <span data-ttu-id="c5276-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5276-126">Requirement</span></span> | <span data-ttu-id="c5276-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c5276-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5276-128">Header</span><span class="sxs-lookup"><span data-stu-id="c5276-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c5276-129"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5276-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5276-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5276-130">Library</span></span><br/> | <dl> <span data-ttu-id="c5276-131"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c5276-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5276-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5276-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5276-133">**CMediaPosition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c5276-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




