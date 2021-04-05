---
title: TCM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für eine Registerkarte in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetItemRect-Makros senden.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- Windows-Steuerelemente für TCM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859198"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="9e6f2-105">TCM \_ GetItemRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9e6f2-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="9e6f2-106">Ruft das umgebende Rechteck für eine Registerkarte in einem Registerkarten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="9e6f2-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="9e6f2-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="9e6f2-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e6f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e6f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e6f2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e6f2-110">Index der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="9e6f2-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="9e6f2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e6f2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e6f2-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck der Registerkarte in viewportkoordinaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="9e6f2-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e6f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e6f2-113">Return value</span></span>

<span data-ttu-id="9e6f2-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9e6f2-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6f2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e6f2-115">Requirements</span></span>



| <span data-ttu-id="9e6f2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e6f2-116">Requirement</span></span> | <span data-ttu-id="9e6f2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9e6f2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6f2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e6f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6f2-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e6f2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e6f2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e6f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6f2-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e6f2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e6f2-122">Header</span><span class="sxs-lookup"><span data-stu-id="9e6f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e6f2-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e6f2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

