---
title: BCM_SETDROPDOWNSTATE Meldung (kommstrg. h)
description: Legt den Dropdown-Zustand für eine Schaltfläche mit dem Dropdown Menü Style tbstyle fest \_ . Senden Sie diese Nachricht explizit oder mithilfe des \_ setdropdownstate-Makros der Schaltfläche.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Windows-Steuerelemente für BCM_SETDROPDOWNSTATE Meldung
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103634"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="197da-105">BCM \_ setdropdownstate-Meldung</span><span class="sxs-lookup"><span data-stu-id="197da-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="197da-106">Legt den Dropdown-Zustand für eine Schaltfläche mit dem [**\_ Dropdown Menü Style tbstyle**](toolbar-control-and-button-styles.md)fest.</span><span class="sxs-lookup"><span data-stu-id="197da-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="197da-107">Senden Sie diese Nachricht explizit oder mithilfe des [**\_ setdropdownstate**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) -Makros der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="197da-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="197da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="197da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="197da-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="197da-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="197da-110">Ein **boolescher** Wert  , der für den Status von BST \_ dropdownpushübertragung true ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="197da-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="197da-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="197da-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="197da-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="197da-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="197da-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="197da-113">Return value</span></span>

<span data-ttu-id="197da-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="197da-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="197da-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="197da-115">Requirements</span></span>



| <span data-ttu-id="197da-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="197da-116">Requirement</span></span> | <span data-ttu-id="197da-117">Wert</span><span class="sxs-lookup"><span data-stu-id="197da-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="197da-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="197da-118">Minimum supported client</span></span><br/> | <span data-ttu-id="197da-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="197da-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="197da-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="197da-120">Minimum supported server</span></span><br/> | <span data-ttu-id="197da-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="197da-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="197da-122">Header</span><span class="sxs-lookup"><span data-stu-id="197da-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="197da-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="197da-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197da-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="197da-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="197da-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="197da-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="197da-126">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="197da-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="197da-127">**Licher**</span><span class="sxs-lookup"><span data-stu-id="197da-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="197da-128">Schaltflächentypen</span><span class="sxs-lookup"><span data-stu-id="197da-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





