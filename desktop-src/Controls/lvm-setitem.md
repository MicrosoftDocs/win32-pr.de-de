---
title: LVM_SETITEM Meldung (kommstrg. h)
description: Legt einige oder alle Attribute eines Listen Ansichts Elements fest. Sie können auch LVM \_ SetItem senden, um den Text eines unter Elements festzulegen. Sie können diese Nachricht explizit oder mithilfe des ListView-Elements "ListView" senden \_ .
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Windows-Steuerelemente für LVM_SETITEM Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040371"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="25160-106">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="25160-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="25160-107">Legt einige oder alle Attribute eines Listen Ansichts Elements fest.</span><span class="sxs-lookup"><span data-stu-id="25160-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="25160-108">Sie können auch LVM \_ SetItem senden, um den Text eines unter Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="25160-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="25160-109">Sie können diese Nachricht explizit oder mithilfe des [**ListView-Elements \_ "ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) " senden.</span><span class="sxs-lookup"><span data-stu-id="25160-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25160-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25160-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25160-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25160-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25160-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="25160-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25160-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25160-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25160-114">Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die die neuen Element Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="25160-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="25160-115">Die Member **iItem** und **iSubItem** identifizieren das Element oder das Unterelement, und das **Masken** Element gibt an, welche Attribute festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25160-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="25160-116">Wenn das **Masken** Element den lvif \_ -Textwert angibt, ist der **pszText** -Member die Adresse einer auf NULL endenden Zeichenfolge, und das **cchtextmax** -Element wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="25160-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="25160-117">Wenn das **Masken** Element den lvif- \_ Zustandswert angibt, gibt der **statemask** -Member an, welche Element Zustände  geändert werden sollen und ob das statusmember die Werte für diese Zustände enthält.</span><span class="sxs-lookup"><span data-stu-id="25160-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25160-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25160-118">Return value</span></span>

<span data-ttu-id="25160-119">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="25160-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="25160-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25160-120">Remarks</span></span>

<span data-ttu-id="25160-121">Um die Attribute eines Listen Ansichts Elements festzulegen, legen Sie den **iItem** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur auf den Index des Elements fest, und legen Sie den **iSubItem** -Member auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="25160-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="25160-122">Für ein Element können Sie die Member **State**, **pszText**, **iImage** und **LPARAM** der **lvitem** -Struktur festlegen.</span><span class="sxs-lookup"><span data-stu-id="25160-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="25160-123">Um den Text eines unter Elements festzulegen, legen Sie die Member **iItem** und **iSubItem** auf das jeweilige Unterelement fest, und verwenden Sie den Member **pszText** , um den Text anzugeben.</span><span class="sxs-lookup"><span data-stu-id="25160-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="25160-124">Alternativ können Sie das [**ListView \_ setitemtext**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) -Makro verwenden, um den Text eines unter Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="25160-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="25160-125">Sie können die **State** -oder **LPARAM** -Member nicht für unter Elemente festlegen, da unter Elemente nicht über diese Attribute verfügen.</span><span class="sxs-lookup"><span data-stu-id="25160-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="25160-126">In Version 4,70 und höher können Sie den **iImage** -Member für unter Elemente festlegen.</span><span class="sxs-lookup"><span data-stu-id="25160-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="25160-127">Das Unterelement-Bild wird angezeigt, wenn das Listenansicht-Steuerelement das erweiterte LVS-Format "from [**\_ \_ subitemimages**](extended-list-view-styles.md) " aufweist.</span><span class="sxs-lookup"><span data-stu-id="25160-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="25160-128">In früheren Versionen wird das Unterelement-Bild ignoriert.</span><span class="sxs-lookup"><span data-stu-id="25160-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="25160-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25160-129">Requirements</span></span>



| <span data-ttu-id="25160-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25160-130">Requirement</span></span> | <span data-ttu-id="25160-131">Wert</span><span class="sxs-lookup"><span data-stu-id="25160-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25160-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25160-132">Minimum supported client</span></span><br/> | <span data-ttu-id="25160-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25160-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25160-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25160-134">Minimum supported server</span></span><br/> | <span data-ttu-id="25160-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25160-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25160-136">Header</span><span class="sxs-lookup"><span data-stu-id="25160-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="25160-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="25160-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="25160-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="25160-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="25160-139">**LVM \_** "S" (Unicode) und " **LVM \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="25160-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





