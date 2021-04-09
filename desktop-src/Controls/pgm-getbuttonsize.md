---
title: PGM_GETBUTTONSIZE Meldung (kommstrg. h)
description: Ruft die aktuelle Schaltflächen Größe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager- \_ getbuttonsize-Makro verwenden.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Windows-Steuerelemente für PGM_GETBUTTONSIZE Meldung
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040797"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="f5d64-105">PGM- \_ getbuttonsize-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f5d64-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="f5d64-106">Ruft die aktuelle Schaltflächen Größe für das Pager-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f5d64-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="f5d64-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ getbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5d64-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5d64-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5d64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d64-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5d64-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f5d64-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f5d64-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f5d64-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5d64-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f5d64-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f5d64-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d64-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5d64-113">Return value</span></span>

<span data-ttu-id="f5d64-114">Gibt einen int-Wert zurück, der die aktuelle Schaltflächen Größe in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="f5d64-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d64-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5d64-115">Requirements</span></span>



| <span data-ttu-id="f5d64-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5d64-116">Requirement</span></span> | <span data-ttu-id="f5d64-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f5d64-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d64-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5d64-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d64-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5d64-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5d64-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5d64-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d64-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5d64-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5d64-122">Header</span><span class="sxs-lookup"><span data-stu-id="f5d64-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d64-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d64-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5d64-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5d64-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d64-125">**PGM \_ setbuttonsize**</span><span class="sxs-lookup"><span data-stu-id="f5d64-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





