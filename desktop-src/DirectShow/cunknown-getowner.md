---
description: Die GetOwner-Methode ruft einen Zeiger auf die IUnknown-Schnittstelle der besitzenden Komponente ab. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls ist die Komponente eigenständig.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Cunknown. GetOwner-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370271"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="ce72f-105">Cunknown. GetOwner-Methode</span><span class="sxs-lookup"><span data-stu-id="ce72f-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="ce72f-106">Die- `GetOwner` Methode ruft einen Zeiger auf die **IUnknown** -Schnittstelle der besitzenden Komponente ab.</span><span class="sxs-lookup"><span data-stu-id="ce72f-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="ce72f-107">Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente.</span><span class="sxs-lookup"><span data-stu-id="ce72f-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="ce72f-108">Andernfalls ist die Komponente eigenständig.</span><span class="sxs-lookup"><span data-stu-id="ce72f-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce72f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce72f-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="ce72f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce72f-110">Parameters</span></span>

<span data-ttu-id="ce72f-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce72f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce72f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce72f-112">Return value</span></span>

<span data-ttu-id="ce72f-113">Gibt einen Zeiger auf die steuernde **IUnknown** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="ce72f-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce72f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce72f-114">Requirements</span></span>



| <span data-ttu-id="ce72f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce72f-115">Requirement</span></span> | <span data-ttu-id="ce72f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ce72f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce72f-117">Header</span><span class="sxs-lookup"><span data-stu-id="ce72f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ce72f-118"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce72f-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce72f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce72f-119">Library</span></span><br/> | <dl> <span data-ttu-id="ce72f-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce72f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




