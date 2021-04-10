---
title: LVM_REDRAWITEMS Meldung (kommstrg. h)
description: Erzwingt, dass ein Listenansicht-Steuerelement einen Bereich von Elementen neu zeichnet. Sie können diese Nachricht explizit oder mithilfe des ListView \_ RedrawItems-Makros senden.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Windows-Steuerelemente für LVM_REDRAWITEMS Meldung
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040589"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="ec7ce-105">LVM \_ RedrawItems-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec7ce-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="ec7ce-106">Erzwingt, dass ein Listenansicht-Steuerelement einen Bereich von Elementen neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="ec7ce-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec7ce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec7ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec7ce-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec7ce-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7ce-110">Der Index des ersten Elements, das neu gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="ec7ce-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec7ce-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7ce-112">Der Index des letzten Elements, das neu gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec7ce-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec7ce-113">Return value</span></span>

<span data-ttu-id="ec7ce-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ec7ce-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7ce-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec7ce-115">Remarks</span></span>

<span data-ttu-id="ec7ce-116">Die angegebenen Elemente werden erst neu gezeichnet, wenn das Listen Ansichts Fenster eine WM-Zeichnungs Nachricht erhält, um Sie neu zu zeichnen. [**\_**](/windows/desktop/gdi/wm-paint)</span><span class="sxs-lookup"><span data-stu-id="ec7ce-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="ec7ce-117">Um sofort neu zu zeichnen, müssen Sie die Funktion [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) aufrufen, nachdem Sie dieses Makro verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7ce-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec7ce-118">Requirements</span></span>



| <span data-ttu-id="ec7ce-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec7ce-119">Requirement</span></span> | <span data-ttu-id="ec7ce-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ec7ce-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7ce-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec7ce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7ce-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec7ce-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec7ce-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec7ce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7ce-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec7ce-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec7ce-125">Header</span><span class="sxs-lookup"><span data-stu-id="ec7ce-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec7ce-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

