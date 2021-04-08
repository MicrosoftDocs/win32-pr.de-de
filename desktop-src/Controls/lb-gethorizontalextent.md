---
title: LB_GETHORIZONTALEXTENT Meldung (Winuser. h)
description: Ruft die Breite in Pixel ab, in der ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann, wenn das Listenfeld eine horizontale Schiebe Leiste hat.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Windows-Steuerelemente für LB_GETHORIZONTALEXTENT Meldung
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957106"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="e5307-104">LB- \_ gethorizontalblock-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e5307-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="e5307-105">Ruft die Breite in Pixel ab, in der ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann, wenn das Listenfeld eine horizontale Schiebe Leiste hat.</span><span class="sxs-lookup"><span data-stu-id="e5307-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5307-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5307-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5307-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5307-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e5307-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e5307-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5307-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5307-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e5307-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5307-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5307-111">Return value</span></span>

<span data-ttu-id="e5307-112">Der Rückgabewert ist die scrollbare Breite des Listen Felds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e5307-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5307-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5307-113">Remarks</span></span>

<span data-ttu-id="e5307-114">Um auf die **lb- \_ gethorizontalblock** -Nachricht zu reagieren, muss das Listenfeld mit dem [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil definiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="e5307-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="e5307-115">Wenn die Anwendung den horizontalen Wertebereich des Listen Felds (mit [**lb- \_ sethorizontalblock**](lb-sethorizontalextent.md)) nicht festgelegt hat, ist der standardmäßige horizontale Block NULL.</span><span class="sxs-lookup"><span data-stu-id="e5307-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="e5307-116">Beachten Sie, dass das Listenfeld den horizontalen Block nicht dynamisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e5307-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5307-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5307-117">Requirements</span></span>



| <span data-ttu-id="e5307-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5307-118">Requirement</span></span> | <span data-ttu-id="e5307-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e5307-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5307-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5307-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e5307-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5307-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5307-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5307-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e5307-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5307-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5307-124">Header</span><span class="sxs-lookup"><span data-stu-id="e5307-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5307-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e5307-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5307-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5307-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5307-127">**LB-Abbild \_ Umfang**</span><span class="sxs-lookup"><span data-stu-id="e5307-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

