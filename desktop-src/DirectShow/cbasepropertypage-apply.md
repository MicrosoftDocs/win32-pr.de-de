---
description: 'Die Apply-Methode wendet die aktuellen Eigenschaften Seiten Werte auf das-Objekt an, das der Eigenschaften Seite zugeordnet ist. Diese Methode implementiert die IPropertyPage:: Apply-Methode.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Cbasepropertypage. Apply-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372563"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="1e660-104">Cbasepropertypage. Apply-Methode</span><span class="sxs-lookup"><span data-stu-id="1e660-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="1e660-105">Die- `Apply` Methode wendet die aktuellen Eigenschaften Seiten Werte auf das-Objekt an, das der Eigenschaften Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1e660-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="1e660-106">Diese Methode implementiert die **IPropertyPage:: apply** -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e660-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e660-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e660-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="1e660-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e660-108">Parameters</span></span>

<span data-ttu-id="1e660-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e660-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e660-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e660-110">Return value</span></span>

<span data-ttu-id="1e660-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e660-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1e660-112">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="1e660-112">Possible values include the following.</span></span>



| <span data-ttu-id="1e660-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1e660-113">Return code</span></span>                                                                                  | <span data-ttu-id="1e660-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e660-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1e660-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1e660-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1e660-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1e660-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="1e660-117"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="1e660-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1e660-118">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1e660-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e660-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e660-119">Remarks</span></span>

<span data-ttu-id="1e660-120">Wenn das [**\_ bdirty-Flag "cbasepropertypage:: m**](cbasepropertypage-m-bdirty.md) " auf " **true**" festgelegt ist, ruft diese Methode die [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="1e660-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="1e660-121">Überschreiben Sie **onapplychanges** , um die Änderungen auf das-Objekt anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="1e660-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e660-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e660-122">Requirements</span></span>



| <span data-ttu-id="1e660-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e660-123">Requirement</span></span> | <span data-ttu-id="1e660-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1e660-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e660-125">Header</span><span class="sxs-lookup"><span data-stu-id="1e660-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1e660-126"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e660-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1e660-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e660-127">Library</span></span><br/> | <dl> <span data-ttu-id="1e660-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1e660-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e660-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e660-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e660-130">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1e660-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




