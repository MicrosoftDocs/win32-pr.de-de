---
description: Übergibt eine an \_ \_ \_ den Filter Diagramm-Manager geänderte Meldung mit einer gewechselten EC-Video Größe.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Cbasecontrolvideo. onvideosizechange-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364424"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="65433-103">Cbasecontrolvideo. onvideosizechange-Methode</span><span class="sxs-lookup"><span data-stu-id="65433-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="65433-104">Übergibt eine an \_ \_ \_ den Filter Diagramm-Manager geänderte Meldung mit einer gewechselten EC-Video Größe.</span><span class="sxs-lookup"><span data-stu-id="65433-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="65433-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65433-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="65433-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65433-106">Parameters</span></span>

<span data-ttu-id="65433-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="65433-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65433-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65433-108">Return value</span></span>

<span data-ttu-id="65433-109">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="65433-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="65433-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="65433-110">Return code</span></span>                                                                                   | <span data-ttu-id="65433-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65433-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="65433-112"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="65433-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="65433-113">Fehler.</span><span class="sxs-lookup"><span data-stu-id="65433-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="65433-114"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="65433-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="65433-115">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="65433-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65433-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65433-116">Remarks</span></span>

<span data-ttu-id="65433-117">Ein Videorenderer sollte diese Member-Funktion jedes Mal, wenn die Videogröße geändert wird, abrufen. Dies wird in der Regel einmal nach der anfänglichen Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="65433-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="65433-118">Wenn der Renderer dynamische Formatänderungen unterstützen kann (von 320 x 240 bis 160 x 120), sollte er nach jeder Änderung auch aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="65433-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="65433-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65433-119">Requirements</span></span>



| <span data-ttu-id="65433-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65433-120">Requirement</span></span> | <span data-ttu-id="65433-121">Wert</span><span class="sxs-lookup"><span data-stu-id="65433-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65433-122">Header</span><span class="sxs-lookup"><span data-stu-id="65433-122">Header</span></span><br/>  | <dl> <span data-ttu-id="65433-123"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65433-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65433-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65433-124">Library</span></span><br/> | <dl> <span data-ttu-id="65433-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="65433-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65433-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65433-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65433-127">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="65433-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




