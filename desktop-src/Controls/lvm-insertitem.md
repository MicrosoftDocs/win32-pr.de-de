---
title: LVM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des ListView \_ InsertItem-Makros senden.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Windows-Steuerelemente für LVM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346748"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="bd0a6-105">LVM \_ InsertItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bd0a6-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="bd0a6-106">Fügt ein neues Element in ein Listenansicht-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="bd0a6-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd0a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd0a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd0a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd0a6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd0a6-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd0a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd0a6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd0a6-112">Ein Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die die Attribute des Listen Ansichts Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="bd0a6-113">Verwenden Sie den **iItem** -Member, um den NULL basierten Index anzugeben, an dem das neue Element eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="bd0a6-114">Wenn dieser Wert größer als die Anzahl der aktuell in der ListView enthaltenen Elemente ist, wird das neue Element an das Ende der Liste angefügt und dem richtigen Index zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="bd0a6-115">Überprüfen Sie den Rückgabewert der Nachricht, um den dem Element zugewiesenen tatsächlichen Index zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd0a6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd0a6-116">Return value</span></span>

<span data-ttu-id="bd0a6-117">Gibt den Index des neuen Elements zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0a6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd0a6-118">Remarks</span></span>

<span data-ttu-id="bd0a6-119">Sie können " [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) " oder " **LVM \_ InsertItem** " nicht verwenden, um unter Elemente einzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="bd0a6-120">Der **iSubItem** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="bd0a6-121">Weitere Informationen zum Festlegen von unter Elementen finden Sie unter [**LVM \_**](lvm-setitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="bd0a6-122">Wenn für ein Listenansicht-Steuerelement die [**LVS \_ Ex- \_ Kontrollkästchen**](extended-list-view-styles.md) festgelegt sind, werden alle Werte, die in Bits 12 bis 15 des **State** -Members der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur platziert werden, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="bd0a6-123">Wenn ein Element mit diesem Stilsatz hinzugefügt wird, wird es immer auf den deaktivierten Zustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="bd0a6-124">Wenn ein Listenansicht-Steuerelement entweder den [**LVS \_ SortAscending**](list-view-window-styles.md) -oder [**LVS \_ sortabsteig**](list-view-window-styles.md) enden Fenster Stil aufweist, schlägt eine **LVM \_ InsertItem** -Nachricht fehl, wenn Sie versuchen, ein Element einzufügen, das LPSTR \_ textcallback als Wert für das zugehörige **pszText** -Element aufweist.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="bd0a6-125">Die **LVM- \_ InsertItem** -Nachricht fügt das neue Element an der richtigen Position in der Sortierreihenfolge ein, wenn die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="bd0a6-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="bd0a6-126">Sie verwenden einen der LVS \_ sortxxx-Stile.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="bd0a6-127">Sie verwenden nicht den [**LVS-Besitzer \_ Zeichnungs**](list-view-window-styles.md) Stil.</span><span class="sxs-lookup"><span data-stu-id="bd0a6-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="bd0a6-128">Der **pszText** -Member der Struktur, auf die von **pitem** gezeigt wird, ist nicht auf "LPSTR textcallback" festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="bd0a6-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="bd0a6-129">Wenn die [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur keine lvif- \_ GroupID im **Mask** -Member enthält, ist der Wert des **igroupid** -Members \_ standardmäßig "groupidcallback".</span><span class="sxs-lookup"><span data-stu-id="bd0a6-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0a6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd0a6-130">Requirements</span></span>



| <span data-ttu-id="bd0a6-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd0a6-131">Requirement</span></span> | <span data-ttu-id="bd0a6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="bd0a6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0a6-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd0a6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0a6-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd0a6-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd0a6-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd0a6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0a6-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd0a6-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd0a6-137">Header</span><span class="sxs-lookup"><span data-stu-id="bd0a6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd0a6-138"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd0a6-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bd0a6-139">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bd0a6-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bd0a6-140">**LVM \_ Insertitemw** (Unicode) und **LVM \_ insertitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bd0a6-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





