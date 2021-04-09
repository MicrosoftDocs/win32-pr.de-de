---
title: TCM_SETCURSEL Meldung (kommstrg. h)
description: Wählt eine Registerkarte in einem Register Steuerelement aus. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ setcurrsel-Makros senden.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Windows-Steuerelemente für TCM_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956496"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="47e4c-105">TCM- \_ setcurrsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="47e4c-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="47e4c-106">Wählt eine Registerkarte in einem Register Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="47e4c-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="47e4c-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ setcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="47e4c-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47e4c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e4c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47e4c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47e4c-110">Index der auszuwählen Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="47e4c-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="47e4c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47e4c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="47e4c-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="47e4c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e4c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47e4c-113">Return value</span></span>

<span data-ttu-id="47e4c-114">Gibt den Index der zuvor ausgewählten Registerkarte zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="47e4c-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="47e4c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47e4c-115">Remarks</span></span>

<span data-ttu-id="47e4c-116">Ein Registerkarten-Steuerelement sendet keinen [TCN \_ selchanging](tcn-selchanging.md) -oder [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Code, wenn mithilfe dieser Meldung eine Registerkarte ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="47e4c-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e4c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47e4c-117">Requirements</span></span>



| <span data-ttu-id="47e4c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47e4c-118">Requirement</span></span> | <span data-ttu-id="47e4c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="47e4c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47e4c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47e4c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="47e4c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47e4c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47e4c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47e4c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="47e4c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47e4c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47e4c-124">Header</span><span class="sxs-lookup"><span data-stu-id="47e4c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e4c-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e4c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





