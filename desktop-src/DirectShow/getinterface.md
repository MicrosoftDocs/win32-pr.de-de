---
description: Die GetInterface-Funktion Ruft einen Schnittstellen Zeiger ab.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface-Funktion (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360962"
---
# <a name="getinterface-function"></a><span data-ttu-id="e0c36-103">GetInterface-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0c36-103">GetInterface function</span></span>

<span data-ttu-id="e0c36-104">Die- `GetInterface` Funktion Ruft einen Schnittstellen Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="e0c36-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0c36-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="e0c36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c36-107">*Kro*</span><span class="sxs-lookup"><span data-stu-id="e0c36-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c36-108">Zeiger auf die **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e0c36-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="e0c36-109">*PPV*</span><span class="sxs-lookup"><span data-stu-id="e0c36-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c36-110">Adresse eines Zeigers auf die abgerufene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e0c36-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c36-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0c36-111">Return value</span></span>

<span data-ttu-id="e0c36-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e0c36-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c36-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0c36-113">Remarks</span></span>

<span data-ttu-id="e0c36-114">Diese Member-Funktion führt ein Thread sicheres Inkrement des Verweis zählungs Elements aus.</span><span class="sxs-lookup"><span data-stu-id="e0c36-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="e0c36-115">Um die Schnittstelle abzurufen und einen Verweis hinzuzufügen, rufen Sie diese Funktion von der über schreibenden Implementierung der **inondelegatingunknown:: nondelegatingqueryinterface** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="e0c36-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c36-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0c36-116">Requirements</span></span>



| <span data-ttu-id="e0c36-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0c36-117">Requirement</span></span> | <span data-ttu-id="e0c36-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e0c36-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c36-119">Header</span><span class="sxs-lookup"><span data-stu-id="e0c36-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e0c36-120"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0c36-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0c36-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0c36-121">Library</span></span><br/> | <dl> <span data-ttu-id="e0c36-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e0c36-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0c36-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0c36-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c36-124">**COM-Hilfsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="e0c36-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="e0c36-125">**Inondelegatingunknown**</span><span class="sxs-lookup"><span data-stu-id="e0c36-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 




