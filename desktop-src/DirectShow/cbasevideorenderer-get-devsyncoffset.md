---
description: Die get \_ devsyncoffset-Methode ruft die Standardabweichung der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem tatsächlichen Rendern ab, seit das Streaming gestartet wurde.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: CBaseVideoRenderer.get_DevSyncOffset-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366954"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="b9241-103">Cbasevideorenderer. get \_ devsyncoffset-Methode</span><span class="sxs-lookup"><span data-stu-id="b9241-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="b9241-104">Die `get_DevSyncOffset` -Methode ruft die Standardabweichung der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem tatsächlichen Rendern ab, seit das Streaming gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9241-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9241-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9241-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="b9241-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9241-107">*pidev*</span><span class="sxs-lookup"><span data-stu-id="b9241-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="b9241-108">Zeiger auf die Standardabweichung der Zeit, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b9241-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9241-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9241-109">Return value</span></span>

<span data-ttu-id="b9241-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b9241-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9241-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9241-111">Remarks</span></span>

<span data-ttu-id="b9241-112">Diese Member-Funktion implementiert die [**iqualprop:: get \_ devsyncoffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b9241-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9241-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9241-113">Requirements</span></span>



| <span data-ttu-id="b9241-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9241-114">Requirement</span></span> | <span data-ttu-id="b9241-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b9241-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9241-116">Header</span><span class="sxs-lookup"><span data-stu-id="b9241-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b9241-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9241-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9241-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9241-118">Library</span></span><br/> | <dl> <span data-ttu-id="b9241-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b9241-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9241-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9241-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9241-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b9241-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




