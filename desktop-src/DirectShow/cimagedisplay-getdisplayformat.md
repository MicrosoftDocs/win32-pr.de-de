---
description: Die getdisplayformat-Methode ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Cimagedisplay. getdisplayformat-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352060"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="ec20c-103">Cimagedisplay. getdisplayformat-Methode</span><span class="sxs-lookup"><span data-stu-id="ec20c-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="ec20c-104">Die- `GetDisplayFormat` Methode ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ec20c-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec20c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec20c-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="ec20c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec20c-106">Parameters</span></span>

<span data-ttu-id="ec20c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ec20c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec20c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec20c-108">Return value</span></span>

<span data-ttu-id="ec20c-109">Gibt einen Zeiger auf eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="ec20c-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec20c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec20c-110">Requirements</span></span>



| <span data-ttu-id="ec20c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec20c-111">Requirement</span></span> | <span data-ttu-id="ec20c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ec20c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec20c-113">Header</span><span class="sxs-lookup"><span data-stu-id="ec20c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ec20c-114"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec20c-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec20c-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec20c-115">Library</span></span><br/> | <dl> <span data-ttu-id="ec20c-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ec20c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec20c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec20c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec20c-118">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ec20c-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




