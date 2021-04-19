---
description: Die onrenderstart-Methode legt Informationen für das Rendering fest.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Cbasevideorenderer. onrenderstart-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360316"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="ff02b-103">Cbasevideorenderer. onrenderstart-Methode</span><span class="sxs-lookup"><span data-stu-id="ff02b-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="ff02b-104">Die- `OnRenderStart` Methode legt Informationen für das Rendering fest.</span><span class="sxs-lookup"><span data-stu-id="ff02b-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff02b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff02b-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="ff02b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff02b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff02b-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="ff02b-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ff02b-108">Zeiger auf das Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="ff02b-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff02b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff02b-109">Return value</span></span>

<span data-ttu-id="ff02b-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ff02b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff02b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff02b-111">Remarks</span></span>

<span data-ttu-id="ff02b-112">Diese Member-Funktion Ruft die aktuelle Uhrzeit aus dem System ab und speichert Sie in einer Element Variablen, die verwendet werden soll, wenn die Zeichnung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="ff02b-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="ff02b-113">Die Funktion führt auch die Leistungs Protokollierung aus.</span><span class="sxs-lookup"><span data-stu-id="ff02b-113">The function also performs performance logging.</span></span> <span data-ttu-id="ff02b-114">Diese Member-Funktion sollte direkt vor dem Zeichnen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ff02b-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="ff02b-115">Diese Member-Funktion überschreibt [**cbaserenderer:: onrenderstart**](cbaserenderer-onrenderstart.md).</span><span class="sxs-lookup"><span data-stu-id="ff02b-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff02b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff02b-116">Requirements</span></span>



| <span data-ttu-id="ff02b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff02b-117">Requirement</span></span> | <span data-ttu-id="ff02b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ff02b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff02b-119">Header</span><span class="sxs-lookup"><span data-stu-id="ff02b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ff02b-120"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff02b-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff02b-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff02b-121">Library</span></span><br/> | <dl> <span data-ttu-id="ff02b-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ff02b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff02b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff02b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff02b-124">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff02b-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




