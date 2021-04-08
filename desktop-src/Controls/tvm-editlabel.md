---
title: TVM_EDITLABEL Meldung (kommstrg. h)
description: Beginnt die direkte Bearbeitung des Texts des angegebenen Elements und ersetzt den Text des Elements durch ein einzeilige Bearbeitungs Steuerelement, das den Text enthält.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Windows-Steuerelemente für TVM_EDITLABEL Meldung
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949692"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="95ac3-104">TVM \_ EditLabel-Meldung</span><span class="sxs-lookup"><span data-stu-id="95ac3-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="95ac3-105">Beginnt die direkte Bearbeitung des Texts des angegebenen Elements und ersetzt den Text des Elements durch ein einzeilige Bearbeitungs Steuerelement, das den Text enthält.</span><span class="sxs-lookup"><span data-stu-id="95ac3-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="95ac3-106">Diese Meldung wählt das angegebene Element implizit aus und konzentriert dieses.</span><span class="sxs-lookup"><span data-stu-id="95ac3-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="95ac3-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="95ac3-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95ac3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95ac3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ac3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95ac3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="95ac3-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="95ac3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="95ac3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95ac3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95ac3-112">Handle für das zu bearbeitende Element.</span><span class="sxs-lookup"><span data-stu-id="95ac3-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ac3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95ac3-113">Return value</span></span>

<span data-ttu-id="95ac3-114">Gibt das Handle für das Bearbeitungs Steuerelement zurück, mit dem der Element Text bei erfolgreicher Bearbeitung bearbeitet wird, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="95ac3-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ac3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95ac3-115">Remarks</span></span>

<span data-ttu-id="95ac3-116">Diese Meldung sendet einen [TVN \_ beginlabeledit](tvn-beginlabeledit.md) -Benachrichtigungs Code an das übergeordnete Element des Strukturansicht-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="95ac3-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="95ac3-117">Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungs Steuerelement zerstört und das Handle ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="95ac3-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="95ac3-118">Sie können das Bearbeitungs Steuerelement Unterklassen, aber nicht zerstören.</span><span class="sxs-lookup"><span data-stu-id="95ac3-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="95ac3-119">Vor dem Senden dieser Nachricht an das-Steuerelement muss das-Steuerelement den Fokus haben.</span><span class="sxs-lookup"><span data-stu-id="95ac3-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="95ac3-120">Der Fokus kann mithilfe der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95ac3-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ac3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95ac3-121">Requirements</span></span>



| <span data-ttu-id="95ac3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95ac3-122">Requirement</span></span> | <span data-ttu-id="95ac3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="95ac3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95ac3-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95ac3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95ac3-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95ac3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95ac3-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95ac3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95ac3-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95ac3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95ac3-128">Header</span><span class="sxs-lookup"><span data-stu-id="95ac3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95ac3-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="95ac3-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="95ac3-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="95ac3-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95ac3-131">**TVM \_ Editlabelw** (Unicode) und **TVM \_ editlabela** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="95ac3-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 

