---
description: 'Die SetObjects-Methode stellt IUnknown-Zeiger für die Objekte bereit, die der Eigenschaften Seite zugeordnet sind. Diese Methode implementiert die IPropertyPage:: abtobjects-Methode.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Cbasepropertypage. * tobjects-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368647"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="3227f-104">Cbasepropertypage. \* tobjects-Methode</span><span class="sxs-lookup"><span data-stu-id="3227f-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="3227f-105">Die- `SetObjects` Methode stellt **IUnknown** -Zeiger für die Objekte bereit, die der Eigenschaften Seite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3227f-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="3227f-106">Diese Methode implementiert die **IPropertyPage:: abtobjects** -Methode.</span><span class="sxs-lookup"><span data-stu-id="3227f-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3227f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3227f-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3227f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3227f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3227f-109">*eines CObject*</span><span class="sxs-lookup"><span data-stu-id="3227f-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="3227f-110">Gibt die Anzahl der **IUnknown** -Zeiger in dem Array an, das von *ppUnk* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3227f-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="3227f-111">*ppUnk*</span><span class="sxs-lookup"><span data-stu-id="3227f-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3227f-112">Gibt ein Array von **IUnknown** -Zeigern an.</span><span class="sxs-lookup"><span data-stu-id="3227f-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3227f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3227f-113">Return value</span></span>

<span data-ttu-id="3227f-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3227f-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3227f-115">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="3227f-115">Possible values include the following.</span></span>



| <span data-ttu-id="3227f-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3227f-116">Return code</span></span>                                                                                  | <span data-ttu-id="3227f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3227f-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3227f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3227f-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3227f-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3227f-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3227f-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3227f-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3227f-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="3227f-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="3227f-122"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="3227f-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="3227f-123">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3227f-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="3227f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3227f-124">Remarks</span></span>

<span data-ttu-id="3227f-125">Obwohl *ppUnk* ein Array von **IUnknown** -Zeigern angibt, ist die **cbasepropertypage** -Klasse nur für die Unterstützung eines zugeordneten Objekts vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="3227f-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="3227f-126">Wenn *CObjects* größer als 1 ist, gibt die Methode E \_ unerwartet zurück.</span><span class="sxs-lookup"><span data-stu-id="3227f-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="3227f-127">Wenn *CObjects* 1 ist, ruft diese Methode die [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3227f-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="3227f-128">Wenn *CObjects* 0 (null) ist, ruft diese Methode die [**cbasepropertypage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3227f-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="3227f-129">Die abgeleitete Klasse sollte beide Methoden überschreiben. Weitere Informationen finden Sie in den Hinweisen zu diesen Methoden.</span><span class="sxs-lookup"><span data-stu-id="3227f-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="3227f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3227f-130">Requirements</span></span>



| <span data-ttu-id="3227f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3227f-131">Requirement</span></span> | <span data-ttu-id="3227f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3227f-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3227f-133">Header</span><span class="sxs-lookup"><span data-stu-id="3227f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3227f-134"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3227f-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3227f-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3227f-135">Library</span></span><br/> | <dl> <span data-ttu-id="3227f-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3227f-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3227f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3227f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3227f-138">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3227f-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




