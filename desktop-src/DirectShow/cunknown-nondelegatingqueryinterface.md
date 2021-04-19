---
description: 'Ruft einen Schnittstellen Zeiger ab und erhöht den Verweis Zähler. Diese Methode implementiert die inondelegatingunknown:: nondelegatingqueryinterface-Methode.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Cunknown. nondelegatingqueryinterface-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362057"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="e4fa6-104">Cunknown. nondelegatingqueryinterface-Methode</span><span class="sxs-lookup"><span data-stu-id="e4fa6-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="e4fa6-105">Ruft einen Schnittstellen Zeiger ab und erhöht den Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="e4fa6-106">Diese Methode implementiert die **inondelegatingunknown:: nondelegatingqueryinterface** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fa6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4fa6-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="e4fa6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4fa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fa6-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="e4fa6-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="e4fa6-110">Der Bezeichner der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e4fa6-111">*PPV*</span><span class="sxs-lookup"><span data-stu-id="e4fa6-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="e4fa6-112">Adresse eines Zeigers, der die Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fa6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4fa6-113">Return value</span></span>

<span data-ttu-id="e4fa6-114">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e4fa6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e4fa6-115">Return code</span></span>                                                                                   | <span data-ttu-id="e4fa6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4fa6-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="e4fa6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fa6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e4fa6-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="e4fa6-119"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fa6-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="e4fa6-120">Diese Schnittstelle wird vom Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="e4fa6-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e4fa6-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e4fa6-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="e4fa6-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4fa6-123">Remarks</span></span>

<span data-ttu-id="e4fa6-124">Die **cunknown** -Klasse macht nur die **iuknown** -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e4fa6-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="e4fa6-125">Überschreiben Sie diese Methode, um zusätzliche Schnittstellen bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="e4fa6-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="e4fa6-126">Informationen dazu, wie Sie diese Methode überschreiben, finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e4fa6-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fa6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4fa6-127">Requirements</span></span>



| <span data-ttu-id="e4fa6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4fa6-128">Requirement</span></span> | <span data-ttu-id="e4fa6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e4fa6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fa6-130">Header</span><span class="sxs-lookup"><span data-stu-id="e4fa6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e4fa6-131"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fa6-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4fa6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4fa6-132">Library</span></span><br/> | <dl> <span data-ttu-id="e4fa6-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fa6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




