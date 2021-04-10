---
title: TVM_SETINDENT Meldung (kommstrg. h)
description: Legt die Breite des Einzugs für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement neu, um die neue Breite widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des TreeView-Makros (TreeView) senden \_ .
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Windows-Steuerelemente für TVM_SETINDENT Meldung
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104180"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="47a5b-105">TVM- \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="47a5b-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="47a5b-106">Legt die Breite des Einzugs für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement neu, um die neue Breite widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="47a5b-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="47a5b-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ -Makros (TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) ) senden.</span><span class="sxs-lookup"><span data-stu-id="47a5b-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47a5b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47a5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47a5b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47a5b-110">Breite des Einzugs in Pixel.</span><span class="sxs-lookup"><span data-stu-id="47a5b-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="47a5b-111">Wenn dieser Parameter kleiner als die vom System definierte Mindestbreite ist, wird die neue Breite auf das vom System definierte Minimalwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47a5b-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="47a5b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47a5b-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="47a5b-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="47a5b-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47a5b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47a5b-114">Return value</span></span>

<span data-ttu-id="47a5b-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="47a5b-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a5b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a5b-116">Remarks</span></span>

<span data-ttu-id="47a5b-117">Der vom System definierte minimale Einzugs Wert ist in der Regel fünf Pixel, aber er ist nicht korrigiert.</span><span class="sxs-lookup"><span data-stu-id="47a5b-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="47a5b-118">Wenn Sie den genauen Wert für den minimalen Einzug auf einem bestimmten System abrufen möchten, senden Sie eine **TVM- \_ setIndent** -Nachricht, bei der *wParam* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="47a5b-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="47a5b-119">Senden Sie dann eine [**TVM- \_ GetIndent**](tvm-getindent.md) -Nachricht, um den minimalen Einzug Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47a5b-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a5b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47a5b-120">Requirements</span></span>



| <span data-ttu-id="47a5b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47a5b-121">Requirement</span></span> | <span data-ttu-id="47a5b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="47a5b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47a5b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47a5b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47a5b-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47a5b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47a5b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47a5b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47a5b-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47a5b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47a5b-127">Header</span><span class="sxs-lookup"><span data-stu-id="47a5b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="47a5b-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="47a5b-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a5b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a5b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a5b-130">**TreeView- \_ Einzug**</span><span class="sxs-lookup"><span data-stu-id="47a5b-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





