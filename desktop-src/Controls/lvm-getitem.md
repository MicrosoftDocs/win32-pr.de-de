---
title: LVM_GETITEM Meldung (kommstrg. h)
description: Ruft einige oder alle der Attribute eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItem-Makros senden.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Windows-Steuerelemente für LVM_GETITEM Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742993"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="fc786-105">LVM- \_ GetItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fc786-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="fc786-106">Ruft einige oder alle der Attribute eines Listen Ansichts Elements ab.</span><span class="sxs-lookup"><span data-stu-id="fc786-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="fc786-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="fc786-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc786-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc786-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc786-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc786-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fc786-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc786-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc786-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc786-112">Ein Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die die Informationen angibt, die abgerufen werden sollen, und Informationen über das Listen Ansichts Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="fc786-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc786-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc786-113">Return value</span></span>

<span data-ttu-id="fc786-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fc786-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc786-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc786-115">Remarks</span></span>

<span data-ttu-id="fc786-116">Wenn die **LVM \_ GetItem** -Nachricht gesendet wird, identifizieren die **iItem** -und **iSubItem** -Member das Element oder Unterelement, über das Informationen abgerufen werden sollen, und das **Masken** Element gibt an, welche Attribute abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc786-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="fc786-117">Eine Liste möglicher Werte finden Sie in der Beschreibung der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc786-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="fc786-118">Wenn das lvif- \_ textflag im **Mask** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur festgelegt ist, muss der **pszText** -Member auf einen gültigen Puffer zeigen, und das **cchtextmax** -Element muss auf die Anzahl der Zeichen in diesem Puffer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fc786-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="fc786-119">Anwendungen sollten nicht davon ausgehen, dass der Text notwendigerweise in den angegebenen Puffer eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fc786-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="fc786-120">Das-Steuerelement kann stattdessen den **pszText** -Member der-Struktur ändern, sodass er auf den neuen Text verweist, anstatt ihn in den Puffer zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="fc786-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="fc786-121">Wenn das **Masken** Element den lvif- \_ Zustandswert angibt, muss der **statemask** -Member die abzurufenden Element Zustands Bits angeben.</span><span class="sxs-lookup"><span data-stu-id="fc786-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="fc786-122">Bei **der Ausgabe** enthält das statusmember die Werte der angegebenen Zustands Bits.</span><span class="sxs-lookup"><span data-stu-id="fc786-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc786-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc786-123">Requirements</span></span>



| <span data-ttu-id="fc786-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc786-124">Requirement</span></span> | <span data-ttu-id="fc786-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fc786-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc786-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc786-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc786-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc786-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc786-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc786-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc786-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc786-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc786-130">Header</span><span class="sxs-lookup"><span data-stu-id="fc786-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc786-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc786-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fc786-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fc786-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fc786-133">**LVM \_ Getitemw** (Unicode) und **LVM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fc786-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





