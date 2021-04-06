---
title: HDM_SETBITMAPMARGIN Meldung (kommstrg. h)
description: Legt die Breite des in Pixel angegebenen Rands einer Bitmap in einem vorhandenen Header Steuerelement fest. Sie können diese Nachricht explizit senden oder das-Header \_ setbitmapmargin-Makro verwenden.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Windows-Steuerelemente für HDM_SETBITMAPMARGIN Meldung
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859128"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="77072-105">HDM- \_ setbitmapmargin-Meldung</span><span class="sxs-lookup"><span data-stu-id="77072-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="77072-106">Legt die Breite des in Pixel angegebenen Rands einer Bitmap in einem vorhandenen Header Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="77072-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="77072-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ setbitmapmargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="77072-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77072-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="77072-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77072-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77072-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77072-110">Die in Pixel angegebene Breite des Randes, das eine Bitmap in einem vorhandenen Header Steuerelement umgibt.</span><span class="sxs-lookup"><span data-stu-id="77072-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="77072-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77072-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="77072-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="77072-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77072-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77072-113">Return value</span></span>

<span data-ttu-id="77072-114">Gibt die Breite des bitmaprandes in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="77072-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="77072-115">Wenn der bitmaprand zuvor nicht angegeben wurde, wird der Standardwert 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ cxedge*) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77072-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="77072-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77072-116">Requirements</span></span>



| <span data-ttu-id="77072-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77072-117">Requirement</span></span> | <span data-ttu-id="77072-118">Wert</span><span class="sxs-lookup"><span data-stu-id="77072-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77072-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77072-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77072-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77072-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77072-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77072-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77072-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77072-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77072-123">Header</span><span class="sxs-lookup"><span data-stu-id="77072-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77072-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="77072-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77072-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77072-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77072-126">**HDM \_ getbitmapmargin**</span><span class="sxs-lookup"><span data-stu-id="77072-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 

