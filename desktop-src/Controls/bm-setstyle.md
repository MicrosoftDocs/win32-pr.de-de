---
title: BM_SETSTYLE Meldung (Winuser. h)
description: Legt den Stil einer Schaltfläche fest. Sie können diese Nachricht explizit senden oder das SetStyle-Makro der Schaltfläche verwenden \_ .
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Windows-Steuerelemente für BM_SETSTYLE Meldung
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949601"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="2cc3c-105">BM- \_ SetStyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2cc3c-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="2cc3c-106">Legt den Stil einer Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-106">Sets the style of a button.</span></span> <span data-ttu-id="2cc3c-107">Sie können diese Nachricht explizit senden oder das [**\_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cc3c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc3c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cc3c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc3c-110">Der Stil der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-110">The button style.</span></span> <span data-ttu-id="2cc3c-111">Dieser Parameter kann eine Kombination von Schaltflächen Stilen sein.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="2cc3c-112">Eine Tabelle mit Schaltflächen Formaten finden Sie unter [Button Styles](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2cc3c-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cc3c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cc3c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc3c-114">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) von *LPARAM* ist ein **boolescher** Wert, der angibt, ob die Schaltfläche neu gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="2cc3c-115">Mit dem Wert **true** wird die Schaltfläche neu gezeichnet. bei einem Wert von **false** wird die Schaltfläche nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc3c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cc3c-116">Return value</span></span>

<span data-ttu-id="2cc3c-117">Diese Meldung gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="2cc3c-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc3c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cc3c-118">Requirements</span></span>



| <span data-ttu-id="2cc3c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cc3c-119">Requirement</span></span> | <span data-ttu-id="2cc3c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2cc3c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc3c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cc3c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc3c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cc3c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cc3c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cc3c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc3c-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cc3c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2cc3c-125">Header</span><span class="sxs-lookup"><span data-stu-id="2cc3c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc3c-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2cc3c-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

