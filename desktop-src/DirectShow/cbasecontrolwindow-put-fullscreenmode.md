---
description: Die Put \_ Fullscreenmode-Methode legt den Vollbildmodus des Renderers fest.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: CBaseControlWindow.put_FullScreenMode-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364722"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="1ff92-103">Cbasecontrolwindow. Put \_ Fullscreenmode-Methode</span><span class="sxs-lookup"><span data-stu-id="1ff92-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="1ff92-104">Die- `put_FullScreenMode` Methode legt den Vollbildmodus des Renderers fest.</span><span class="sxs-lookup"><span data-stu-id="1ff92-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ff92-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="1ff92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ff92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff92-107">*Fullscreenmode*</span><span class="sxs-lookup"><span data-stu-id="1ff92-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff92-108">Der anzuwendende Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="1ff92-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff92-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ff92-109">Return value</span></span>

<span data-ttu-id="1ff92-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1ff92-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ff92-111">Die aktuelle Implementierung gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="1ff92-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff92-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ff92-112">Remarks</span></span>

<span data-ttu-id="1ff92-113">Ein Videorenderer, der einen Vollbildmodus implementiert, sollte diese Element Funktion überschreiben und alle unterstützten Modi implementieren.</span><span class="sxs-lookup"><span data-stu-id="1ff92-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff92-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ff92-114">Requirements</span></span>



| <span data-ttu-id="1ff92-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ff92-115">Requirement</span></span> | <span data-ttu-id="1ff92-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1ff92-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff92-117">Header</span><span class="sxs-lookup"><span data-stu-id="1ff92-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1ff92-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ff92-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ff92-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ff92-119">Library</span></span><br/> | <dl> <span data-ttu-id="1ff92-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1ff92-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff92-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ff92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff92-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1ff92-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




