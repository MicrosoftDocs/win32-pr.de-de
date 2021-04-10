---
title: HDM_GETBITMAPMARGIN Meldung (kommstrg. h)
description: Ruft die Breite des bitmaprandes für ein Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ getbitmapmargin-Makro verwenden.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Windows-Steuerelemente für HDM_GETBITMAPMARGIN Meldung
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956508"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="e0eda-105">HDM \_ getbitmapmargin-Meldung</span><span class="sxs-lookup"><span data-stu-id="e0eda-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="e0eda-106">Ruft die Breite des bitmaprandes für ein Header Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="e0eda-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="e0eda-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ getbitmapmargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0eda-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0eda-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0eda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0eda-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0eda-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e0eda-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e0eda-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e0eda-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0eda-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e0eda-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e0eda-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0eda-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0eda-113">Return value</span></span>

<span data-ttu-id="e0eda-114">Gibt die Breite des bitmaprandes in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="e0eda-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="e0eda-115">Wenn der bitmaprand zuvor nicht angegeben wurde, wird der Standardwert 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ cxedge) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0eda-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0eda-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0eda-116">Requirements</span></span>



| <span data-ttu-id="e0eda-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0eda-117">Requirement</span></span> | <span data-ttu-id="e0eda-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e0eda-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0eda-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0eda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0eda-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0eda-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0eda-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0eda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0eda-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0eda-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0eda-123">Header</span><span class="sxs-lookup"><span data-stu-id="e0eda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0eda-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0eda-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0eda-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0eda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0eda-126">**HDM \_ setbitmapmargin**</span><span class="sxs-lookup"><span data-stu-id="e0eda-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 

