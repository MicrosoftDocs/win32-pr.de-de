---
title: WM_MENUDRAG Meldung (Winuser. h)
description: Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menü Element zieht.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346769"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="72a9e-104">WM- \_ menudrag-Meldung</span><span class="sxs-lookup"><span data-stu-id="72a9e-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="72a9e-105">Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menü Element zieht.</span><span class="sxs-lookup"><span data-stu-id="72a9e-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="72a9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72a9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72a9e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72a9e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72a9e-108">Die Position des Elements, an dem der Zieh Vorgang begonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="72a9e-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="72a9e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72a9e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72a9e-110">Ein Handle für das Menü, das das Element enthält.</span><span class="sxs-lookup"><span data-stu-id="72a9e-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72a9e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72a9e-111">Return value</span></span>

<span data-ttu-id="72a9e-112">Die Anwendung muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="72a9e-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="72a9e-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="72a9e-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="72a9e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72a9e-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72a9e-115"><dt>**MND \_ Fortsetzen**</dt> von <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="72a9e-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="72a9e-116">Das Menü sollte aktiv bleiben.</span><span class="sxs-lookup"><span data-stu-id="72a9e-116">Menu should remain active.</span></span> <span data-ttu-id="72a9e-117">Wenn die Maus losgelassen wird, sollte Sie ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="72a9e-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="72a9e-118"><dt>**MND \_ Endmenu**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="72a9e-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="72a9e-119">Das Menü sollte beendet werden.</span><span class="sxs-lookup"><span data-stu-id="72a9e-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="72a9e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72a9e-120">Remarks</span></span>

<span data-ttu-id="72a9e-121">Die Anwendung kann die [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) -Funktion als Reaktion auf diese Nachricht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="72a9e-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="72a9e-122">Um ein Drag & Drop-Menü zu erstellen, rufen Sie [**setmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) mit **MNS \_ DragDrop** auf.</span><span class="sxs-lookup"><span data-stu-id="72a9e-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a9e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72a9e-123">Requirements</span></span>



| <span data-ttu-id="72a9e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72a9e-124">Requirement</span></span> | <span data-ttu-id="72a9e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="72a9e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a9e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72a9e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="72a9e-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72a9e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="72a9e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72a9e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="72a9e-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72a9e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72a9e-130">Header</span><span class="sxs-lookup"><span data-stu-id="72a9e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="72a9e-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="72a9e-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a9e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72a9e-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="72a9e-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="72a9e-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72a9e-134">**Setmenuinfo**</span><span class="sxs-lookup"><span data-stu-id="72a9e-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="72a9e-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="72a9e-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="72a9e-136">Menüs</span><span class="sxs-lookup"><span data-stu-id="72a9e-136">Menus</span></span>](menus.md)
</dt> </dl>

 

