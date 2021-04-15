---
title: TVM_ENDEDITLABELNOW Meldung (kommstrg. h)
description: Beendet die Bearbeitung der Bezeichnung eines Struktur Ansichts Elements. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "tdeditlabelnow" senden.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Windows-Steuerelemente für TVM_ENDEDITLABELNOW Meldung
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517588"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="f2834-105">TVM- \_ Meldung "tdeditlabelnow"</span><span class="sxs-lookup"><span data-stu-id="f2834-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="f2834-106">Beendet die Bearbeitung der Bezeichnung eines Struktur Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="f2834-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="f2834-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ tdeditlabelnow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) " senden.</span><span class="sxs-lookup"><span data-stu-id="f2834-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2834-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2834-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2834-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2834-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2834-110">Eine Variable, die angibt, ob die Bearbeitung abgebrochen wird, ohne dass Sie in der Bezeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f2834-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="f2834-111">Wenn dieser Parameter **true** ist, bricht das System die Bearbeitung ab, ohne die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f2834-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="f2834-112">Andernfalls speichert das System die Änderungen an der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="f2834-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="f2834-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2834-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f2834-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f2834-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2834-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2834-115">Return value</span></span>

<span data-ttu-id="f2834-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f2834-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2834-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2834-117">Remarks</span></span>

<span data-ttu-id="f2834-118">Diese Meldung bewirkt, dass der [TVN \_ endlabeledit](tvn-endlabeledit.md) -Benachrichtigungs Code an das übergeordnete Fenster des Strukturansicht-Steuer Elements gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2834-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2834-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2834-119">Requirements</span></span>



| <span data-ttu-id="f2834-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2834-120">Requirement</span></span> | <span data-ttu-id="f2834-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f2834-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2834-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2834-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f2834-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2834-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2834-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2834-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f2834-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2834-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2834-126">Header</span><span class="sxs-lookup"><span data-stu-id="f2834-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2834-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2834-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





