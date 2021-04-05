---
title: LB_SETHORIZONTALEXTENT Meldung (Winuser. h)
description: Legt die Breite (in Pixel) fest, um die ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann.
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Windows-Steuerelemente für LB_SETHORIZONTALEXTENT Meldung
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859163"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="f6953-104">LB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="f6953-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="f6953-105">Legt die Breite (in Pixel) fest, um die ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6953-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="f6953-106">Wenn die Breite des Listen Felds kleiner als dieser Wert ist, führt die horizontale Schiebe Leiste einen horizontalen Bildlauf durch Elemente im Listenfeld aus.</span><span class="sxs-lookup"><span data-stu-id="f6953-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="f6953-107">Wenn die Breite des Listen Felds größer oder gleich diesem Wert ist, wird die horizontale Schiebe Leiste ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="f6953-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6953-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6953-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6953-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6953-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6953-110">Gibt die Anzahl der Pixel an, um die das Listenfeld gescrollt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6953-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="f6953-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f6953-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="f6953-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6953-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6953-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6953-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6953-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6953-114">Return value</span></span>

<span data-ttu-id="f6953-115">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6953-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6953-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6953-116">Remarks</span></span>

<span data-ttu-id="f6953-117">Um auf die **lb- \_ lthorizontalblock** -Nachricht zu reagieren, muss das Listenfeld mit dem [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil definiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="f6953-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="f6953-118">Beachten Sie, dass ein Listenfeld seinen horizontalen Block nicht dynamisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f6953-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="f6953-119">Diese Meldung hat keine Auswirkung auf ein Listenfeld mit mehreren Spalten.</span><span class="sxs-lookup"><span data-stu-id="f6953-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6953-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6953-120">Requirements</span></span>



| <span data-ttu-id="f6953-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6953-121">Requirement</span></span> | <span data-ttu-id="f6953-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f6953-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6953-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6953-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f6953-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6953-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6953-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6953-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f6953-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6953-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6953-127">Header</span><span class="sxs-lookup"><span data-stu-id="f6953-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6953-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f6953-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6953-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6953-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6953-130">**LB- \_ gethorizontalblock**</span><span class="sxs-lookup"><span data-stu-id="f6953-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

