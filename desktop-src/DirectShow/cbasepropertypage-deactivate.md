---
description: Die Methode zum Deaktivieren zerstört das Dialogfenster. Diese Methode implementiert die IPropertyPage::D eaktivierungs-Methode.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Cbasepropertypage. deaktiviert-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369116"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="eba18-104">Cbasepropertypage. deaktivieren-Methode</span><span class="sxs-lookup"><span data-stu-id="eba18-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="eba18-105">Mit der- `Deactivate` Methode wird das Dialogfeld zerstört.</span><span class="sxs-lookup"><span data-stu-id="eba18-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="eba18-106">Diese Methode implementiert die **IPropertyPage::D eaktivierungs** -Methode.</span><span class="sxs-lookup"><span data-stu-id="eba18-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba18-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eba18-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="eba18-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eba18-108">Parameters</span></span>

<span data-ttu-id="eba18-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eba18-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eba18-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eba18-110">Return value</span></span>

<span data-ttu-id="eba18-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eba18-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eba18-112">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="eba18-112">Possible values include the following.</span></span>



| <span data-ttu-id="eba18-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eba18-113">Return code</span></span>                                                                                  | <span data-ttu-id="eba18-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eba18-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="eba18-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eba18-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="eba18-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eba18-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="eba18-117"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="eba18-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="eba18-118">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="eba18-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eba18-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eba18-119">Requirements</span></span>



| <span data-ttu-id="eba18-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eba18-120">Requirement</span></span> | <span data-ttu-id="eba18-121">Wert</span><span class="sxs-lookup"><span data-stu-id="eba18-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba18-122">Header</span><span class="sxs-lookup"><span data-stu-id="eba18-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eba18-123"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eba18-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="eba18-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eba18-124">Library</span></span><br/> | <dl> <span data-ttu-id="eba18-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eba18-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eba18-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eba18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba18-127">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eba18-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="eba18-128">**Cbasepropertypage:: ondeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="eba18-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




