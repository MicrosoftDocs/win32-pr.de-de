---
description: Mit der Unregister-Methode wird der Filter aus der Registrierung entfernt.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Cbasefilter. Unregister-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370042"
---
# <a name="cbasefilterunregister-method"></a><span data-ttu-id="803fe-103">Cbasefilter. Unregister-Methode</span><span class="sxs-lookup"><span data-stu-id="803fe-103">CBaseFilter.Unregister method</span></span>

<span data-ttu-id="803fe-104">Die- `Unregister` Methode entfernt den Filter aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="803fe-104">The `Unregister` method removes the filter from the registry.</span></span>

> [!Note]  
> <span data-ttu-id="803fe-105">Diese Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="803fe-105">This method is obsolete.</span></span> <span data-ttu-id="803fe-106">Die Registrierung neuer Filter sollte mithilfe der [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="803fe-106">New filters should be unregistered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="803fe-107">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="803fe-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="803fe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="803fe-108">Syntax</span></span>


```C++
HRESULT Unregister();
```



## <a name="parameters"></a><span data-ttu-id="803fe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="803fe-109">Parameters</span></span>

<span data-ttu-id="803fe-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="803fe-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="803fe-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="803fe-111">Return value</span></span>

<span data-ttu-id="803fe-112">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="803fe-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="803fe-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="803fe-113">Requirements</span></span>



| <span data-ttu-id="803fe-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="803fe-114">Requirement</span></span> | <span data-ttu-id="803fe-115">Wert</span><span class="sxs-lookup"><span data-stu-id="803fe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="803fe-116">Header</span><span class="sxs-lookup"><span data-stu-id="803fe-116">Header</span></span><br/>  | <dl> <span data-ttu-id="803fe-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="803fe-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="803fe-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="803fe-118">Library</span></span><br/> | <dl> <span data-ttu-id="803fe-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="803fe-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803fe-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="803fe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803fe-121">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="803fe-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




