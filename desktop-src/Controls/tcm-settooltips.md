---
title: TCM_SETTOOLTIPS Meldung (kommstrg. h)
description: Weist einem Registerkarten-Steuerelement ein ToolTip-Steuerelement zu. Sie können diese Nachricht explizit oder mithilfe des tabctrl- \_ Makros SetToolTips senden.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Windows-Steuerelemente für TCM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739872"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="44ced-105">TCM- \_ SetToolTips-Meldung</span><span class="sxs-lookup"><span data-stu-id="44ced-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="44ced-106">Weist einem Registerkarten-Steuerelement ein ToolTip-Steuerelement zu.</span><span class="sxs-lookup"><span data-stu-id="44ced-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="44ced-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Makros \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) senden.</span><span class="sxs-lookup"><span data-stu-id="44ced-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="44ced-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="44ced-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44ced-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44ced-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44ced-110">Handle für das QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="44ced-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="44ced-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44ced-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="44ced-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="44ced-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44ced-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44ced-113">Return value</span></span>

<span data-ttu-id="44ced-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="44ced-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ced-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44ced-115">Remarks</span></span>

<span data-ttu-id="44ced-116">Sie können das QuickInfo-Steuerelement, das einem Registerkarten-Steuerelement zugeordnet ist, mithilfe der [**TCM \_ gettooltips**](tcm-gettooltips.md) -Nachricht abrufen</span><span class="sxs-lookup"><span data-stu-id="44ced-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ced-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44ced-117">Requirements</span></span>



| <span data-ttu-id="44ced-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44ced-118">Requirement</span></span> | <span data-ttu-id="44ced-119">Wert</span><span class="sxs-lookup"><span data-stu-id="44ced-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44ced-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44ced-120">Minimum supported client</span></span><br/> | <span data-ttu-id="44ced-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44ced-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44ced-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44ced-122">Minimum supported server</span></span><br/> | <span data-ttu-id="44ced-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44ced-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44ced-124">Header</span><span class="sxs-lookup"><span data-stu-id="44ced-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ced-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ced-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





