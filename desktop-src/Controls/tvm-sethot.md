---
title: TVM_SETHOT Meldung (kommstrg. h)
description: Legt das heiße Element für ein Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView-Makros "-Host" senden \_ .
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Windows-Steuerelemente für TVM_SETHOT Meldung
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957036"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="cf222-105">TVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="cf222-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="cf222-106">\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="cf222-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="cf222-107">Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="cf222-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="cf222-108">Legt das heiße Element für ein Strukturansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="cf222-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="cf222-109">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) -Makros "-Host" senden.</span><span class="sxs-lookup"><span data-stu-id="cf222-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf222-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf222-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf222-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf222-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf222-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="cf222-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cf222-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf222-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf222-114">Handle für das neue heiße Element.</span><span class="sxs-lookup"><span data-stu-id="cf222-114">Handle to the new hot item.</span></span> <span data-ttu-id="cf222-115">Wenn dieser Wert **null** ist, wird für das Strukturansicht-Steuerelement festgelegt, dass kein heißes Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cf222-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf222-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf222-116">Return value</span></span>

<span data-ttu-id="cf222-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="cf222-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="cf222-118">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cf222-118">Security Considerations</span></span>

<span data-ttu-id="cf222-119">Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="cf222-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf222-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf222-120">Remarks</span></span>

<span data-ttu-id="cf222-121">Das *heiße Element* ist das Element, auf das der Mauszeiger zeigt.</span><span class="sxs-lookup"><span data-stu-id="cf222-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="cf222-122">Mit dieser Meldung wird ein Element so aussehen, als wäre es das heiße Element, auch wenn der Mauszeiger nicht darauf zeigt.</span><span class="sxs-lookup"><span data-stu-id="cf222-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="cf222-123">Diese Meldung hat keinen sichtbaren Effekt, wenn der Stil für die [**TV- \_ trackselect**](tree-view-control-window-styles.md) -Einstellung nicht festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="cf222-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="cf222-124">Wenn dies erfolgreich ist, bewirkt diese Meldung, dass das heiße Element neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="cf222-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="cf222-125">Diese Meldung wird ignoriert, wenn *LPARAM* den Wert **null** hat und das Strukturansicht-Steuerelement die Maus nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="cf222-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf222-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf222-126">Requirements</span></span>



| <span data-ttu-id="cf222-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf222-127">Requirement</span></span> | <span data-ttu-id="cf222-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cf222-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf222-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf222-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf222-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf222-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf222-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf222-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf222-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf222-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf222-133">Header</span><span class="sxs-lookup"><span data-stu-id="cf222-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf222-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf222-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf222-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf222-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf222-136">**TreeView \_ -Element**</span><span class="sxs-lookup"><span data-stu-id="cf222-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





