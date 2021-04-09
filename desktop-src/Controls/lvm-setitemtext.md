---
title: LVM_SETITEMTEXT Meldung (kommstrg. h)
description: Ändert den Text eines Listen Ansichts Elements oder unter Elements. Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" mit dem Text "ListView" senden \_ .
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Windows-Steuerelemente für LVM_SETITEMTEXT Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858940"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="d3e27-105">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="d3e27-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="d3e27-106">Ändert den Text eines Listen Ansichts Elements oder unter Elements.</span><span class="sxs-lookup"><span data-stu-id="d3e27-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="d3e27-107">Sie können diese Nachricht explizit oder mithilfe des ListView-Objekts "" mit dem [**\_ Text "ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) " senden.</span><span class="sxs-lookup"><span data-stu-id="d3e27-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3e27-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3e27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e27-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3e27-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3e27-110">Der null basierte Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="d3e27-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="d3e27-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3e27-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3e27-112">Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d3e27-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="d3e27-113">Der **iSubItem** -Member ist der Index des unter Elements, oder er kann NULL sein, um die Element Bezeichnung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3e27-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="d3e27-114">Der **pszText** -Member ist die Adresse einer null-terminierten Zeichenfolge, die den neuen Text enthält. Er kann auch **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d3e27-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="d3e27-115">Der **pszText** -Member kann auch LPSTR \_ textcallback sein, um ein Rückruf Element anzugeben, für das das übergeordnete Fenster den Text speichert.</span><span class="sxs-lookup"><span data-stu-id="d3e27-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="d3e27-116">In diesem Fall sendet das Listenansicht-Steuerelement einen [**LVN \_ getdispinfo**](lvn-getdispinfo.md) -Benachrichtigungs Code, wenn er den Text benötigt.</span><span class="sxs-lookup"><span data-stu-id="d3e27-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e27-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3e27-117">Return value</span></span>

<span data-ttu-id="d3e27-118">Wenn Sie diese Meldung explizit senden, wird **true** zurückgegeben, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d3e27-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e27-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3e27-119">Requirements</span></span>



| <span data-ttu-id="d3e27-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3e27-120">Requirement</span></span> | <span data-ttu-id="d3e27-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d3e27-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e27-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3e27-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e27-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e27-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3e27-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3e27-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e27-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e27-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3e27-126">Header</span><span class="sxs-lookup"><span data-stu-id="d3e27-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e27-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e27-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d3e27-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d3e27-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d3e27-129">**LVM \_** "S" (Unicode) und " **LVM" \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d3e27-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





