---
description: 'CBaseDispatch.GetTypeInfo-Methode: Die GetTypeInfo-Methode ruft die Typinformationen für das Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.'
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: CBaseDispatch.GetTypeInfo-Methode (Ctlutil.h)
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
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120118"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="9169c-103">CBaseDispatch.GetTypeInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="9169c-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="9169c-104">Die `GetTypeInfo` -Methode ruft die Typinformationen für das -Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9169c-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9169c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9169c-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="9169c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9169c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9169c-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="9169c-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="9169c-108">Verweis auf einen Schnittstellenbezeichner (IID), der die Schnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="9169c-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="9169c-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="9169c-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9169c-110">Geben Sie informationen ein, die sie zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9169c-110">Type information to return.</span></span> <span data-ttu-id="9169c-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9169c-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9169c-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="9169c-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="9169c-113">Gebietsschemabezeichner</span><span class="sxs-lookup"><span data-stu-id="9169c-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9169c-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="9169c-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9169c-115">Adresse einer Variablen, die einen **ITypeInfo-Zeiger** empfängt.</span><span class="sxs-lookup"><span data-stu-id="9169c-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9169c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9169c-116">Return value</span></span>

<span data-ttu-id="9169c-117">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="9169c-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9169c-118">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="9169c-118">Possible values include the following.</span></span>



| <span data-ttu-id="9169c-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9169c-119">Return code</span></span>                                                                                             | <span data-ttu-id="9169c-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9169c-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9169c-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9169c-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="9169c-122">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9169c-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="9169c-123"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="9169c-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="9169c-124"> NULL-Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="9169c-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="9169c-125"><dt>**TYP \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="9169c-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="9169c-126">Der *itinfo-Parameter* ist nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9169c-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9169c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9169c-127">Remarks</span></span>

<span data-ttu-id="9169c-128">Diese Methode verhält sich wie die **IDispatch::GetTypeInfo-Methode.**</span><span class="sxs-lookup"><span data-stu-id="9169c-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="9169c-129">Sie enthält jedoch einen zusätzlichen Parameter, *riid,* der die Schnittstelle angibt, für die Typinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9169c-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9169c-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9169c-130">Requirements</span></span>



| <span data-ttu-id="9169c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9169c-131">Requirement</span></span> | <span data-ttu-id="9169c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9169c-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9169c-133">Header</span><span class="sxs-lookup"><span data-stu-id="9169c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9169c-134"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9169c-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9169c-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9169c-135">Library</span></span><br/> | <dl> <span data-ttu-id="9169c-136"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9169c-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9169c-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9169c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9169c-138">**CBaseDispatch-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9169c-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




