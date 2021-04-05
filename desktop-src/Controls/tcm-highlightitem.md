---
title: TCM_HIGHLIGHTITEM Meldung (kommstrg. h)
description: Legt den Hervorhebungs Zustand eines Registerkarten Elements fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ highlightitem-Makros senden.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Windows-Steuerelemente für TCM_HIGHLIGHTITEM Meldung
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859194"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="d32b2-105">TCM \_ highlightitem-Meldung</span><span class="sxs-lookup"><span data-stu-id="d32b2-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="d32b2-106">Legt den Hervorhebungs Zustand eines Registerkarten Elements fest.</span><span class="sxs-lookup"><span data-stu-id="d32b2-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="d32b2-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ highlightitem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d32b2-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d32b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d32b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d32b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d32b2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d32b2-110">Ein **int** -Wert, der den NULL basierten Index eines Registerkarten-Steuer Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="d32b2-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="d32b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d32b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d32b2-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der den festzulegenden Hervorhebungs Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="d32b2-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="d32b2-113">Wenn dieser Wert **true** ist, wird die Registerkarte hervorgehoben. Wenn der Wert **false** ist, wird die Registerkarte auf den Standardzustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d32b2-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="d32b2-114">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d32b2-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d32b2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d32b2-115">Return value</span></span>

<span data-ttu-id="d32b2-116">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="d32b2-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d32b2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d32b2-117">Remarks</span></span>

<span data-ttu-id="d32b2-118">In Comctl32.dll Version 6,0 hat diese Nachricht keine sichtbare Auswirkung, wenn ein Design aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d32b2-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d32b2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d32b2-119">Requirements</span></span>



| <span data-ttu-id="d32b2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d32b2-120">Requirement</span></span> | <span data-ttu-id="d32b2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d32b2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d32b2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d32b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d32b2-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d32b2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d32b2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d32b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d32b2-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d32b2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d32b2-126">Header</span><span class="sxs-lookup"><span data-stu-id="d32b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d32b2-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d32b2-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

