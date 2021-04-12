---
title: LVM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das QuickInfo-Steuerelement ab, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ gettooltips-Makro verwenden.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Windows-Steuerelemente für LVM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478510"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="a059c-105">LVM \_ gettooltips-Meldung</span><span class="sxs-lookup"><span data-stu-id="a059c-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="a059c-106">Ruft das QuickInfo-Steuerelement ab, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a059c-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="a059c-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ gettooltips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="a059c-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a059c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a059c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a059c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a059c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a059c-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a059c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a059c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a059c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a059c-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a059c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a059c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a059c-113">Return value</span></span>

<span data-ttu-id="a059c-114">Gibt das Handle des QuickInfo-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="a059c-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a059c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a059c-115">Requirements</span></span>



| <span data-ttu-id="a059c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a059c-116">Requirement</span></span> | <span data-ttu-id="a059c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a059c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a059c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a059c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a059c-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a059c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a059c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a059c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a059c-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a059c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a059c-122">Header</span><span class="sxs-lookup"><span data-stu-id="a059c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a059c-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a059c-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a059c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a059c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a059c-125">**LVM- \_ SetToolTips**</span><span class="sxs-lookup"><span data-stu-id="a059c-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





