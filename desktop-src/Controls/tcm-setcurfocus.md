---
title: TCM_SETCURFOCUS Meldung (kommstrg. h)
description: Legt den Fokus auf eine angegebene Registerkarte in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ setcurrfocus-Makros senden.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Windows-Steuerelemente für TCM_SETCURFOCUS Meldung
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956497"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="1caad-105">TCM- \_ setcurrfocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1caad-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="1caad-106">Legt den Fokus auf eine angegebene Registerkarte in einem Registerkarten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="1caad-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="1caad-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ setcurrfocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="1caad-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1caad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1caad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1caad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1caad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1caad-110">Der Index der Registerkarte, die den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="1caad-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="1caad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1caad-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1caad-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1caad-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1caad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1caad-113">Return value</span></span>

<span data-ttu-id="1caad-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1caad-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1caad-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1caad-115">Remarks</span></span>

<span data-ttu-id="1caad-116">Wenn das Registerkarten-Steuerelement den [**TCS \_ -Schalt**](tab-control-styles.md) Flächen Stil (Schaltflächen Modus) aufweist, kann sich die Registerkarte mit dem Fokus von der ausgewählten Registerkarte unterscheiden. Wenn z. b. eine Registerkarte ausgewählt ist, kann der Benutzer die Pfeiltasten drücken, um den Fokus auf eine andere Registerkarte festzulegen, ohne die ausgewählte Registerkarte zu ändern. Im Schaltflächen Modus legt **TCM \_ setcurrfocus** den Eingabefokus auf die Schaltfläche fest, die der angegebenen Registerkarte zugeordnet ist, aber die ausgewählte Registerkarte wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="1caad-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="1caad-117">Wenn das Registerkarten-Steuerelement nicht über die [**TCS- \_ Schalt**](tab-control-styles.md) Flächen verfügt, wird durch das Ändern des Fokus auch die ausgewählte Registerkarte geändert. In diesem Fall sendet das Registerkarten-Steuer [Element die TCN \_ selchanging](tcn-selchanging.md) -und [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Codes an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="1caad-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1caad-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1caad-118">Requirements</span></span>



| <span data-ttu-id="1caad-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1caad-119">Requirement</span></span> | <span data-ttu-id="1caad-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1caad-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1caad-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1caad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1caad-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1caad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1caad-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1caad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1caad-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1caad-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1caad-125">Header</span><span class="sxs-lookup"><span data-stu-id="1caad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1caad-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1caad-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1caad-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1caad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1caad-128">**TCM \_ getcurrfocus**</span><span class="sxs-lookup"><span data-stu-id="1caad-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 





