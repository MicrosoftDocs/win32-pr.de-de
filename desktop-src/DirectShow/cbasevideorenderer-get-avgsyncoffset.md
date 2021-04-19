---
description: Die get \_ avgsyncoffset-Methode ruft den Durchschnitt der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem Zeitpunkt ab, zu dem das Streaming tatsächlich für alle Frames gerendert wurde.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: CBaseVideoRenderer.get_AvgSyncOffset-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357609"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="ea2be-103">Cbasevideorenderer. get \_ avgsyncoffset-Methode</span><span class="sxs-lookup"><span data-stu-id="ea2be-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="ea2be-104">Die `get_AvgSyncOffset` -Methode ruft den Durchschnitt der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem Zeitpunkt ab, zu dem das Streaming tatsächlich für alle Frames gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="ea2be-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea2be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea2be-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="ea2be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea2be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea2be-107">*piavg*</span><span class="sxs-lookup"><span data-stu-id="ea2be-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2be-108">Zeiger auf den Durchschnitt der Zeit, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea2be-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea2be-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea2be-109">Return value</span></span>

<span data-ttu-id="ea2be-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ea2be-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea2be-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea2be-111">Remarks</span></span>

<span data-ttu-id="ea2be-112">Diese Member-Funktion implementiert die [**iqualprop:: get \_ avgsyncoffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ea2be-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea2be-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea2be-113">Requirements</span></span>



| <span data-ttu-id="ea2be-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea2be-114">Requirement</span></span> | <span data-ttu-id="ea2be-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ea2be-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2be-116">Header</span><span class="sxs-lookup"><span data-stu-id="ea2be-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ea2be-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea2be-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea2be-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea2be-118">Library</span></span><br/> | <dl> <span data-ttu-id="ea2be-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ea2be-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea2be-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea2be-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea2be-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea2be-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




