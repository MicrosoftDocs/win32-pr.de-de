---
title: TVM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Teilt dem Strukturansicht-Steuerelement mit, dass erweiterte Stile festgelegt werden. Senden Sie diese Nachricht, oder verwenden Sie das Makro TreeView-Element "- \_ textendedstyle".
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Windows-Steuerelemente für TVM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517957"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="6c9cd-105">TVM- \_ Meldung "abtextendedstyle"</span><span class="sxs-lookup"><span data-stu-id="6c9cd-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="6c9cd-106">Teilt dem Strukturansicht-Steuerelement mit, dass erweiterte Stile festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c9cd-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="6c9cd-107">Senden Sie diese Nachricht, oder verwenden Sie das Makro TreeView-Element "- [**\_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)".</span><span class="sxs-lookup"><span data-stu-id="6c9cd-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="6c9cd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c9cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c9cd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c9cd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c9cd-110">Maske, die verwendet wird, um die festzulegenden Stile auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6c9cd-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="6c9cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c9cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c9cd-112">Der-Wert, der den erweiterten Stil angibt.</span><span class="sxs-lookup"><span data-stu-id="6c9cd-112">Value that indicates the extended style.</span></span> <span data-ttu-id="6c9cd-113">Weitere Informationen zu Stilen finden Sie Unterstruktur [Ansicht-Steuerelement erweiterte Stile](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6c9cd-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c9cd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c9cd-114">Return value</span></span>

<span data-ttu-id="6c9cd-115">Wenn diese Nachricht erfolgreich ist, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c9cd-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c9cd-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c9cd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c9cd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c9cd-117">Remarks</span></span>

<span data-ttu-id="6c9cd-118">Die erweiterten Stile für ein Strukturansicht-Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c9cd-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9cd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c9cd-119">Requirements</span></span>



| <span data-ttu-id="6c9cd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c9cd-120">Requirement</span></span> | <span data-ttu-id="6c9cd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9cd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9cd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c9cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9cd-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c9cd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c9cd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c9cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9cd-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c9cd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c9cd-126">Header</span><span class="sxs-lookup"><span data-stu-id="6c9cd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c9cd-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c9cd-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

