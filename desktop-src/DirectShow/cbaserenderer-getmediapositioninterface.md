---
description: Die getmediapositioninterface-Methode ruft die imediaposition-und imediaseeking-Schnittstellen Zeiger des Filters ab.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Cbaserderderer. getmediapositioninterface-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352877"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="89c78-103">Cbaserderderer. getmediapositioninterface-Methode</span><span class="sxs-lookup"><span data-stu-id="89c78-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="89c78-104">Die `GetMediaPositionInterface` -Methode ruft die [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstellen Zeiger des Filters ab.</span><span class="sxs-lookup"><span data-stu-id="89c78-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="89c78-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="89c78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89c78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c78-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="89c78-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="89c78-108">Verweis Bezeichner der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="89c78-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="89c78-109">*PPV*</span><span class="sxs-lookup"><span data-stu-id="89c78-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="89c78-110">Adresse einer Variablen, die den Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="89c78-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c78-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89c78-111">Return value</span></span>

<span data-ttu-id="89c78-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89c78-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="89c78-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="89c78-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="89c78-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="89c78-114">Return code</span></span>                                                                                   | <span data-ttu-id="89c78-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89c78-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="89c78-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89c78-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="89c78-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="89c78-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="89c78-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="89c78-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="89c78-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="89c78-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="89c78-120"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="89c78-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="89c78-121">Schnittstelle wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89c78-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89c78-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89c78-122">Remarks</span></span>

<span data-ttu-id="89c78-123">Der Filter delegiert alle Suchbefehle an ein [**crendererpospassthru**](crendererpospassthru.md) -Objekt, das Sie per Upstream übergibt.</span><span class="sxs-lookup"><span data-stu-id="89c78-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="89c78-124">Diese Methode erstellt das **crendererpospassthru** -Objekt, wenn es noch nicht vorhanden ist, und fragt es nach der angeforderten Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="89c78-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="89c78-125">Die Element Variable [**cbaserenderer:: m \_ pposition**](cbaserenderer-m-pposition.md) speichert einen Zeiger auf das **crendererpospassthru** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="89c78-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c78-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89c78-126">Requirements</span></span>



| <span data-ttu-id="89c78-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89c78-127">Requirement</span></span> | <span data-ttu-id="89c78-128">Wert</span><span class="sxs-lookup"><span data-stu-id="89c78-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c78-129">Header</span><span class="sxs-lookup"><span data-stu-id="89c78-129">Header</span></span><br/>  | <dl> <span data-ttu-id="89c78-130"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89c78-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89c78-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89c78-131">Library</span></span><br/> | <dl> <span data-ttu-id="89c78-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="89c78-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89c78-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89c78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c78-134">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="89c78-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




