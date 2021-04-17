---
title: PGM_RECALCSIZE Meldung (kommstrg. h)
description: Erzwingt die Neuberechnung der Größe des enthaltenen Fensters durch das Pager-Steuerelement. Das Senden dieser Nachricht führt dazu, dass eine PGN \_ calcsize-Benachrichtigung gesendet wird. Sie können diese Nachricht explizit senden oder das Pager \_ recalcsize-Makro verwenden.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Windows-Steuerelemente für PGM_RECALCSIZE Meldung
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476311"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="fcf2e-106">PGM- \_ Nachricht "recalcsize"</span><span class="sxs-lookup"><span data-stu-id="fcf2e-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="fcf2e-107">Erzwingt die Neuberechnung der Größe des enthaltenen Fensters durch das Pager-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="fcf2e-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="fcf2e-108">Das Senden dieser Nachricht führt dazu, dass eine [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcf2e-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="fcf2e-109">Sie können diese Nachricht explizit senden oder das [**Pager \_ recalcsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="fcf2e-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcf2e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcf2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf2e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcf2e-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fcf2e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fcf2e-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fcf2e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcf2e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fcf2e-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fcf2e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf2e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcf2e-115">Return value</span></span>

<span data-ttu-id="fcf2e-116">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcf2e-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf2e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcf2e-117">Requirements</span></span>



| <span data-ttu-id="fcf2e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcf2e-118">Requirement</span></span> | <span data-ttu-id="fcf2e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fcf2e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf2e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcf2e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf2e-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcf2e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcf2e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcf2e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf2e-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcf2e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcf2e-124">Header</span><span class="sxs-lookup"><span data-stu-id="fcf2e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf2e-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf2e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





