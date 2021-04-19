---
description: Die \_ Methode Get Caption Ruft die aktuelle Fenster Beschriftung ab.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: CBaseControlWindow.get_Caption-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359308"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="d0af3-103">Cbasecontrolwindow. get \_ Caption-Methode</span><span class="sxs-lookup"><span data-stu-id="d0af3-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="d0af3-104">Die- `get_Caption` Methode ruft die aktuelle Fenster Beschriftung ab.</span><span class="sxs-lookup"><span data-stu-id="d0af3-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0af3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0af3-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="d0af3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0af3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0af3-107">*pstrincaption*</span><span class="sxs-lookup"><span data-stu-id="d0af3-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="d0af3-108">Zeiger auf die aktuelle Fenster Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="d0af3-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0af3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0af3-109">Return value</span></span>

<span data-ttu-id="d0af3-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d0af3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0af3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0af3-111">Remarks</span></span>

<span data-ttu-id="d0af3-112">Den meisten Fenstern der obersten Ebene auf einem Windows-basierten Desktop ist ein Titel (Beschriftung) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d0af3-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="d0af3-113">Diese Eigenschaft kann durch die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle abgefragt und festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0af3-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="d0af3-114">Jeder Beschriftungs Satz ist nur sichtbar, wenn für das Fenster der WS- \_ Beschriftungs Stil angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d0af3-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="d0af3-115">Wenn dies nicht der Fall ist, kann die Beschriftung weiterhin festgelegt (und abgerufen) werden, auch wenn Sie für den Benutzer nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="d0af3-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0af3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0af3-116">Requirements</span></span>



| <span data-ttu-id="d0af3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0af3-117">Requirement</span></span> | <span data-ttu-id="d0af3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d0af3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0af3-119">Header</span><span class="sxs-lookup"><span data-stu-id="d0af3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d0af3-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0af3-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0af3-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d0af3-121">Library</span></span><br/> | <dl> <span data-ttu-id="d0af3-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d0af3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0af3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0af3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0af3-124">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d0af3-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




