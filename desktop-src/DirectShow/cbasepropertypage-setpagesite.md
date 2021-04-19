---
description: 'Die setpagesite-Methode initialisiert die Eigenschaften Seite und stellt einen Zeiger auf die ipropertypagesite-Schnittstelle des Eigenschaften Frames bereit. Diese Methode implementiert die IPropertyPage:: setpagesite-Methode.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Cbasepropertypage. setpagesite-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370984"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="996f0-104">Cbasepropertypage. setpagesite-Methode</span><span class="sxs-lookup"><span data-stu-id="996f0-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="996f0-105">Die `SetPageSite` -Methode initialisiert die Eigenschaften Seite und stellt einen Zeiger auf die **ipropertypagesite** -Schnittstelle des Eigenschaften Frames bereit.</span><span class="sxs-lookup"><span data-stu-id="996f0-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="996f0-106">Diese Methode implementiert die **IPropertyPage:: setpagesite** -Methode.</span><span class="sxs-lookup"><span data-stu-id="996f0-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="996f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="996f0-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="996f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="996f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996f0-109">*ppagesite*</span><span class="sxs-lookup"><span data-stu-id="996f0-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="996f0-110">Zeiger auf die **ipropertypagesite** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="996f0-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996f0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="996f0-111">Return value</span></span>

<span data-ttu-id="996f0-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="996f0-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="996f0-113">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="996f0-113">Possible values include the following.</span></span>



| <span data-ttu-id="996f0-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="996f0-114">Return code</span></span>                                                                                  | <span data-ttu-id="996f0-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="996f0-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="996f0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="996f0-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="996f0-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="996f0-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="996f0-118"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="996f0-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="996f0-119">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="996f0-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="996f0-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="996f0-120">Remarks</span></span>

<span data-ttu-id="996f0-121">Die-Methode speichert den *ppagesite* -Zeiger in der Member-Variable [**cbasepropertypage:: m \_ ppagesite**](cbasepropertypage-m-ppagesite.md) .</span><span class="sxs-lookup"><span data-stu-id="996f0-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="996f0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="996f0-122">Requirements</span></span>



| <span data-ttu-id="996f0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="996f0-123">Requirement</span></span> | <span data-ttu-id="996f0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="996f0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996f0-125">Header</span><span class="sxs-lookup"><span data-stu-id="996f0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="996f0-126"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="996f0-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="996f0-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="996f0-127">Library</span></span><br/> | <dl> <span data-ttu-id="996f0-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="996f0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996f0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="996f0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996f0-130">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="996f0-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




