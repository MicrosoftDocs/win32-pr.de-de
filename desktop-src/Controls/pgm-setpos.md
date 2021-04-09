---
title: PGM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle Bild Lauf Position für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ SetPos-Makro verwenden.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Windows-Steuerelemente für PGM_SETPOS Meldung
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741224"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="3064e-105">PGM- \_ SetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3064e-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="3064e-106">Legt die aktuelle Bild Lauf Position für das Pager-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="3064e-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="3064e-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="3064e-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3064e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3064e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3064e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3064e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3064e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3064e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3064e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3064e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3064e-112">Der Wert vom Typ " **int** ", der die neue Scrollposition enthält, in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3064e-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3064e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3064e-113">Return value</span></span>

<span data-ttu-id="3064e-114">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3064e-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3064e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3064e-115">Requirements</span></span>



| <span data-ttu-id="3064e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3064e-116">Requirement</span></span> | <span data-ttu-id="3064e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3064e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3064e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3064e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3064e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3064e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3064e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3064e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3064e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3064e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3064e-122">Header</span><span class="sxs-lookup"><span data-stu-id="3064e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3064e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3064e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





