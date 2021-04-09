---
title: TVM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für ein Struktur Ansichts Element ab und gibt an, ob das Element sichtbar ist. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemRect-Makros senden.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Windows-Steuerelemente für TVM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103462"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="89001-105">TVM- \_ GetItemRect-Meldung</span><span class="sxs-lookup"><span data-stu-id="89001-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="89001-106">Ruft das umgebende Rechteck für ein Struktur Ansichts Element ab und gibt an, ob das Element sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="89001-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="89001-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="89001-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="89001-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89001-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89001-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89001-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89001-110">Ein-Wert, der den Teil des Elements angibt, für den das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="89001-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="89001-111">Wenn dieser Parameter **true** ist, enthält das umgebende Rechteck nur den Text des Elements.</span><span class="sxs-lookup"><span data-stu-id="89001-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="89001-112">Andernfalls enthält Sie die gesamte Zeile, die das Element im Strukturansicht-Steuerelement einnimmt.</span><span class="sxs-lookup"><span data-stu-id="89001-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="89001-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89001-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89001-114">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die beim Senden der Nachricht das Handle des Elements enthält, für das das Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="89001-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="89001-115">Im folgenden Beispiel finden Sie weitere Informationen dazu, wie Sie das Element Handle in diesem Parameter platzieren.</span><span class="sxs-lookup"><span data-stu-id="89001-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="89001-116">Nachdem die Nachricht zurückgegeben wurde, enthält dieser Parameter das umgebende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="89001-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="89001-117">Die Koordinaten sind relativ zur linken oberen Ecke des Strukturansicht-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="89001-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89001-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89001-118">Return value</span></span>

<span data-ttu-id="89001-119">Wenn das Element sichtbar ist und das umgebende Rechteck erfolgreich abgerufen wurde, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="89001-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="89001-120">Andernfalls gibt die Nachricht **false** zurück und ruft das umgebende Rechteck nicht ab.</span><span class="sxs-lookup"><span data-stu-id="89001-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="89001-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89001-121">Remarks</span></span>

<span data-ttu-id="89001-122">Beim Senden dieser Nachricht enthält der *LPARAM* -Parameter das Handle des Elements, für das das Rechteck abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="89001-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="89001-123">Das Handle wird in *LPARAM* platziert, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="89001-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="89001-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89001-124">Requirements</span></span>



| <span data-ttu-id="89001-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89001-125">Requirement</span></span> | <span data-ttu-id="89001-126">Wert</span><span class="sxs-lookup"><span data-stu-id="89001-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89001-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89001-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89001-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89001-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89001-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89001-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89001-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89001-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89001-131">Header</span><span class="sxs-lookup"><span data-stu-id="89001-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="89001-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="89001-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

