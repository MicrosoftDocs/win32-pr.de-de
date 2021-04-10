---
title: PGM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ SetBkColor-Makro verwenden.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Windows-Steuerelemente für PGM_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103479"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="e0346-105">PGM- \_ SetBkColor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e0346-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="e0346-106">Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="e0346-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="e0346-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0346-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0346-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0346-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0346-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0346-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e0346-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e0346-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e0346-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0346-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0346-112">**COLORREF** -Wert, der die neue Hintergrundfarbe des Pager-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="e0346-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0346-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0346-113">Return value</span></span>

<span data-ttu-id="e0346-114">Gibt einen **COLORREF** -Wert zurück, der die vorherige Hintergrundfarbe enthält.</span><span class="sxs-lookup"><span data-stu-id="e0346-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0346-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0346-115">Remarks</span></span>

<span data-ttu-id="e0346-116">Standardmäßig verwendet das Pager-Steuerelement die Vordergrundfarbe der System Schaltfläche als Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="e0346-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="e0346-117">Dies ist die gleiche Farbe, die durch den Aufruf von [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) mit Color \_ btnface abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e0346-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0346-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0346-118">Requirements</span></span>



| <span data-ttu-id="e0346-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0346-119">Requirement</span></span> | <span data-ttu-id="e0346-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e0346-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0346-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0346-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0346-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0346-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0346-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0346-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0346-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0346-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0346-125">Header</span><span class="sxs-lookup"><span data-stu-id="e0346-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0346-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0346-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

