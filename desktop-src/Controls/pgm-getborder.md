---
title: PGM_GETBORDER Meldung (kommstrg. h)
description: Ruft die aktuelle Rahmengröße für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager- \_ GetBorder-Makro verwenden.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Windows-Steuerelemente für PGM_GETBORDER Meldung
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339996"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="453ad-105">PGM \_ GetBorder-Nachricht</span><span class="sxs-lookup"><span data-stu-id="453ad-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="453ad-106">Ruft die aktuelle Rahmengröße für das Pager-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="453ad-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="453ad-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="453ad-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="453ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="453ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="453ad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="453ad-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="453ad-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="453ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="453ad-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="453ad-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="453ad-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="453ad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="453ad-113">Return value</span></span>

<span data-ttu-id="453ad-114">Gibt einen int-Wert zurück, der die aktuelle Rahmengröße in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="453ad-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="453ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="453ad-115">Requirements</span></span>



| <span data-ttu-id="453ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="453ad-116">Requirement</span></span> | <span data-ttu-id="453ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="453ad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="453ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="453ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="453ad-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="453ad-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="453ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="453ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="453ad-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="453ad-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="453ad-122">Header</span><span class="sxs-lookup"><span data-stu-id="453ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="453ad-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="453ad-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="453ad-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="453ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453ad-125">**PGM- \_ setborder**</span><span class="sxs-lookup"><span data-stu-id="453ad-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 





