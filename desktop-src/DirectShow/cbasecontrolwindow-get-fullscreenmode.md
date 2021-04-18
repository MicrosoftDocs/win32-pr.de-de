---
description: Die get \_ Fullscreenmode-Methode ruft den aktuellen Vollbildmodus ab.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: CBaseControlWindow.get_FullScreenMode-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354666"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="ccdf0-103">Cbasecontrolwindow. get \_ Fullscreenmode-Methode</span><span class="sxs-lookup"><span data-stu-id="ccdf0-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="ccdf0-104">Die- `get_FullScreenMode` Methode ruft den aktuellen Vollbildmodus ab.</span><span class="sxs-lookup"><span data-stu-id="ccdf0-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccdf0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccdf0-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="ccdf0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccdf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccdf0-107">*Fullscreenmode*</span><span class="sxs-lookup"><span data-stu-id="ccdf0-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="ccdf0-108">Zeiger auf den aktuellen Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="ccdf0-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccdf0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccdf0-109">Return value</span></span>

<span data-ttu-id="ccdf0-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ccdf0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccdf0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccdf0-111">Remarks</span></span>

<span data-ttu-id="ccdf0-112">Diese Member-Funktion gibt \_ standardmäßig E notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="ccdf0-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="ccdf0-113">Dadurch wird dem [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Plug-in-Verteiler mitgeteilt, dass dieser Renderer keinen Vollbild-Renderer implementiert.</span><span class="sxs-lookup"><span data-stu-id="ccdf0-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccdf0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccdf0-114">Requirements</span></span>



| <span data-ttu-id="ccdf0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccdf0-115">Requirement</span></span> | <span data-ttu-id="ccdf0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ccdf0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccdf0-117">Header</span><span class="sxs-lookup"><span data-stu-id="ccdf0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ccdf0-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccdf0-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ccdf0-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ccdf0-119">Library</span></span><br/> | <dl> <span data-ttu-id="ccdf0-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ccdf0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccdf0-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccdf0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccdf0-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ccdf0-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




