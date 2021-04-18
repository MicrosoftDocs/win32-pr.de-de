---
description: 'Die QueryId-Methode ruft den PIN-Bezeichner ab. Diese Methode implementiert die IPin:: QueryId-Methode.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Cbasepin. QueryId-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364719"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="dde41-104">Cbasepin. QueryId-Methode</span><span class="sxs-lookup"><span data-stu-id="dde41-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="dde41-105">Die- `QueryId` Methode ruft den PIN-Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="dde41-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="dde41-106">Diese Methode implementiert die [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dde41-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dde41-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="dde41-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dde41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde41-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="dde41-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="dde41-110">Zeiger auf den PIN-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dde41-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde41-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dde41-111">Return value</span></span>

<span data-ttu-id="dde41-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dde41-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dde41-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="dde41-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="dde41-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dde41-114">Return code</span></span>                                                                                   | <span data-ttu-id="dde41-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dde41-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dde41-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dde41-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dde41-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="dde41-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="dde41-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dde41-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dde41-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="dde41-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="dde41-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="dde41-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dde41-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="dde41-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dde41-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dde41-122">Remarks</span></span>

<span data-ttu-id="dde41-123">Diese Methode gibt eine Kopie der [**cbasepin:: m \_ PName**](cbasepin-m-pname.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="dde41-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde41-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dde41-124">Requirements</span></span>



| <span data-ttu-id="dde41-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dde41-125">Requirement</span></span> | <span data-ttu-id="dde41-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dde41-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde41-127">Header</span><span class="sxs-lookup"><span data-stu-id="dde41-127">Header</span></span><br/>  | <dl> <span data-ttu-id="dde41-128"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dde41-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dde41-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dde41-129">Library</span></span><br/> | <dl> <span data-ttu-id="dde41-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dde41-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde41-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dde41-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde41-132">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dde41-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




