---
title: TVM_SETITEMHEIGHT Meldung (kommstrg. h)
description: Legt die Höhe der Elemente in der Strukturansicht fest. Sie können diese Nachricht explizit oder mithilfe des TreeView-Objekts " \_ abtitemheight" senden.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Windows-Steuerelemente für TVM_SETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956630"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="a086b-105">TVM-Meldung "". \_</span><span class="sxs-lookup"><span data-stu-id="a086b-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="a086b-106">Legt die Höhe der Elemente in der Strukturansicht fest.</span><span class="sxs-lookup"><span data-stu-id="a086b-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="a086b-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Objekts " \_ abtitemheight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) " senden.</span><span class="sxs-lookup"><span data-stu-id="a086b-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a086b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a086b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a086b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a086b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a086b-110">Die neue Höhe jedes Elements in der Strukturansicht in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a086b-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="a086b-111">Höhen, die kleiner als 1 sind, werden auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a086b-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="a086b-112">Wenn dieses Argument nicht gerade ist und das Strukturansicht-Steuerelement nicht über den nicht- [**\_ evenheight**](tree-view-control-window-styles.md) -Stil des Fernseh Baums verfügt, wird dieser Wert auf den nächstgelegenen geraden Wert gerundet.</span><span class="sxs-lookup"><span data-stu-id="a086b-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="a086b-113">Wenn dieses Argument-1 ist, wird das Steuerelement auf seine Standardelement Höhe zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a086b-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="a086b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a086b-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a086b-115">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a086b-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a086b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a086b-116">Return value</span></span>

<span data-ttu-id="a086b-117">Gibt die vorherige Höhe der Elemente in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="a086b-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="a086b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a086b-118">Remarks</span></span>

<span data-ttu-id="a086b-119">Das Strukturansicht-Steuerelement verwendet diesen Wert für die Höhe aller Elemente.</span><span class="sxs-lookup"><span data-stu-id="a086b-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="a086b-120">Informationen zum Ändern der Höhe einzelner Elemente finden Sie in der Beschreibung des **iintegral** -Members der [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a086b-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a086b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a086b-121">Requirements</span></span>



| <span data-ttu-id="a086b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a086b-122">Requirement</span></span> | <span data-ttu-id="a086b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a086b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a086b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a086b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a086b-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a086b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a086b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a086b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a086b-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a086b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a086b-128">Header</span><span class="sxs-lookup"><span data-stu-id="a086b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a086b-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a086b-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a086b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a086b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a086b-131">**TVM \_ GetItemHeight**</span><span class="sxs-lookup"><span data-stu-id="a086b-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





