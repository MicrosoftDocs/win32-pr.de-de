---
title: TCM_DESELECTALL Meldung (kommstrg. h)
description: Setzt Elemente in einem Registerkarten-Steuerelement zurück und löscht alle, die auf den tcis- \_ ButtonPressed-Zustand festgelegt wurden. Sie können diese Nachricht explizit oder mithilfe des tabctrl- \_ Makros DeselectAll senden.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Windows-Steuerelemente für TCM_DESELECTALL Meldung
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105747"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="50404-105">TCM- \_ DeselectAll-Nachricht</span><span class="sxs-lookup"><span data-stu-id="50404-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="50404-106">Setzt Elemente in einem Registerkarten-Steuerelement zurück und löscht alle, die auf den [**tcis- \_ ButtonPressed**](tab-control-item-states.md) -Zustand festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="50404-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="50404-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Makros \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) senden.</span><span class="sxs-lookup"><span data-stu-id="50404-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="50404-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50404-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50404-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50404-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50404-110">Flag, das den Gültigkeitsbereich der Elementauswahl angibt.</span><span class="sxs-lookup"><span data-stu-id="50404-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="50404-111">Wenn dieser Parameter auf **false** festgelegt ist, werden alle Registerkarten Elemente zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="50404-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="50404-112">Wenn der Wert auf **true** festgelegt ist, werden alle Registerkarten Elemente mit Ausnahme der aktuell ausgewählten Elemente zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="50404-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="50404-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50404-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="50404-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="50404-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50404-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50404-115">Return value</span></span>

<span data-ttu-id="50404-116">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="50404-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="50404-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50404-117">Remarks</span></span>

<span data-ttu-id="50404-118">Diese Meldung ist nur dann sinnvoll, wenn das Style-Flag der [**TCS- \_ Schalt**](tab-control-styles.md) Flächen festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="50404-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="50404-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50404-119">Requirements</span></span>



| <span data-ttu-id="50404-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50404-120">Requirement</span></span> | <span data-ttu-id="50404-121">Wert</span><span class="sxs-lookup"><span data-stu-id="50404-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50404-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50404-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50404-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50404-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50404-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50404-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50404-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50404-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50404-126">Header</span><span class="sxs-lookup"><span data-stu-id="50404-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50404-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="50404-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





