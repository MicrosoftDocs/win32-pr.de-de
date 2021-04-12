---
title: TCM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das QuickInfo-Steuerelement ab, das einem Register Steuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ gettooltips-Makros senden.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Windows-Steuerelemente für TCM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105735"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="dd810-105">TCM \_ gettooltips-Meldung</span><span class="sxs-lookup"><span data-stu-id="dd810-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="dd810-106">Ruft das Handle für das QuickInfo-Steuerelement ab, das einem Register Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dd810-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="dd810-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ gettooltips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="dd810-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd810-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd810-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd810-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd810-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dd810-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="dd810-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dd810-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd810-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd810-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="dd810-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd810-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd810-113">Return value</span></span>

<span data-ttu-id="dd810-114">Gibt das Handle für das QuickInfo-Steuerelement zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="dd810-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd810-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd810-115">Remarks</span></span>

<span data-ttu-id="dd810-116">Ein Registerkarten-Steuerelement erstellt ein QuickInfo-Steuerelement, wenn es den [**TCS- \_ Tooltips**](tab-control-styles.md) -Stil</span><span class="sxs-lookup"><span data-stu-id="dd810-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="dd810-117">Sie können einem Registerkarten-Steuerelement auch ein QuickInfo-Steuerelement mithilfe der [**TCM- \_ SetToolTips**](tcm-settooltips.md) -Nachricht zuweisen.</span><span class="sxs-lookup"><span data-stu-id="dd810-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd810-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd810-118">Requirements</span></span>



| <span data-ttu-id="dd810-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd810-119">Requirement</span></span> | <span data-ttu-id="dd810-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dd810-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd810-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd810-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd810-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd810-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd810-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd810-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd810-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd810-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd810-125">Header</span><span class="sxs-lookup"><span data-stu-id="dd810-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd810-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd810-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





