---
description: Die Register-Methode fügt den Filter der Registrierung hinzu.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Cbasefilter. Register-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361651"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="0f809-103">Cbasefilter. Register-Methode</span><span class="sxs-lookup"><span data-stu-id="0f809-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="0f809-104">Die- `Register` Methode fügt den Filter der Registrierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f809-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="0f809-105">Diese Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0f809-105">This method is obsolete.</span></span> <span data-ttu-id="0f809-106">Neue Filter sollten mithilfe der [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="0f809-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="0f809-107">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0f809-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0f809-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f809-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="0f809-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f809-109">Parameters</span></span>

<span data-ttu-id="0f809-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f809-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f809-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f809-111">Return value</span></span>

<span data-ttu-id="0f809-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0f809-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="0f809-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0f809-113">Return code</span></span>                                                                             | <span data-ttu-id="0f809-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f809-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="0f809-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f809-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0f809-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0f809-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="0f809-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0f809-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0f809-118">Es sind keine Registrierungsinformationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f809-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f809-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f809-119">Requirements</span></span>



| <span data-ttu-id="0f809-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f809-120">Requirement</span></span> | <span data-ttu-id="0f809-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0f809-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f809-122">Header</span><span class="sxs-lookup"><span data-stu-id="0f809-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0f809-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f809-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f809-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f809-124">Library</span></span><br/> | <dl> <span data-ttu-id="0f809-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f809-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f809-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f809-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f809-127">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f809-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




