---
description: 'Die GetPageInfo-Methode ruft Informationen zur Eigenschaften Seite ab. Diese Methode implementiert die IPropertyPage:: getpagumfo-Methode.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Cbasepropertypage. getpagumfo-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369173"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="76d6c-104">Cbasepropertypage. getpagumfo-Methode</span><span class="sxs-lookup"><span data-stu-id="76d6c-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="76d6c-105">Die- `GetPageInfo` Methode ruft Informationen zur Eigenschaften Seite ab.</span><span class="sxs-lookup"><span data-stu-id="76d6c-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="76d6c-106">Diese Methode implementiert die **IPropertyPage:: getpagumfo** -Methode.</span><span class="sxs-lookup"><span data-stu-id="76d6c-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d6c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76d6c-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="76d6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76d6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d6c-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="76d6c-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="76d6c-110">Zeiger auf eine vom Aufrufer zugewiesene **PROPPAGEINFO** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="76d6c-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d6c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76d6c-111">Return value</span></span>

<span data-ttu-id="76d6c-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="76d6c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="76d6c-113">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="76d6c-113">Possible values include the following.</span></span>



| <span data-ttu-id="76d6c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76d6c-114">Return code</span></span>                                                                                   | <span data-ttu-id="76d6c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76d6c-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="76d6c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76d6c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="76d6c-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="76d6c-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="76d6c-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="76d6c-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="76d6c-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="76d6c-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="76d6c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76d6c-120">Requirements</span></span>



| <span data-ttu-id="76d6c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76d6c-121">Requirement</span></span> | <span data-ttu-id="76d6c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="76d6c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d6c-123">Header</span><span class="sxs-lookup"><span data-stu-id="76d6c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="76d6c-124"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76d6c-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="76d6c-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76d6c-125">Library</span></span><br/> | <dl> <span data-ttu-id="76d6c-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="76d6c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d6c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76d6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d6c-128">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="76d6c-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




