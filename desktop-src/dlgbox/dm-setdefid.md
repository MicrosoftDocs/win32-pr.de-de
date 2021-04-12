---
title: DM_SETDEFID Meldung (Winuser. h)
description: Ändert den Bezeichner der Standard-pushschaltfläche für ein Dialogfeld.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Dialog Felder DM_SETDEFID Meldung
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518878"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="e6514-104">DM \_ -setdefid-Meldung</span><span class="sxs-lookup"><span data-stu-id="e6514-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="e6514-105">Ändert den Bezeichner der Standard-pushschaltfläche für ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e6514-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="e6514-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6514-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6514-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6514-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6514-108">Der Bezeichner eines Push Button-Steuer Elements, das zum Standard wird.</span><span class="sxs-lookup"><span data-stu-id="e6514-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="e6514-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6514-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6514-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6514-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6514-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6514-111">Return value</span></span>

<span data-ttu-id="e6514-112">Der Rückgabewert ist immer " **true**".</span><span class="sxs-lookup"><span data-stu-id="e6514-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6514-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6514-113">Remarks</span></span>

<span data-ttu-id="e6514-114">Diese Meldung wird von der [**defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) -Funktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e6514-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="e6514-115">Um die Standard Schaltfläche Push festzulegen, kann die Funktion die Nachrichten [**WM \_ getdlgcode**](wm-getdlgcode.md) und [**BM \_ SetStyle**](../controls/bm-setstyle.md) an das angegebene Steuerelement und die aktuelle Standard-Schaltfläche Push senden.</span><span class="sxs-lookup"><span data-stu-id="e6514-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="e6514-116">Die Verwendung der **DM \_ setdefid-** Nachricht kann dazu führen, dass mehr als eine Schaltfläche den Standardzustand der pushschaltfläche aufweist.</span><span class="sxs-lookup"><span data-stu-id="e6514-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="e6514-117">Wenn das System ein Dialogfeld öffnet, wird die erste Schaltfläche "Push" in der Dialogfeld Vorlage mit dem standardmäßigen Zustands Rahmen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e6514-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="e6514-118">Durch das Senden einer **DM \_ setdefid-** Meldung zum Ändern der Standard Schaltfläche wird nicht immer der standardmäßige Zustands Rahmen aus der ersten Schaltfläche "Push" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e6514-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="e6514-119">In diesen Fällen sollte die Anwendung eine BM- [**\_ SetStyle**](../controls/bm-setstyle.md) -Nachricht senden, um die Rahmenart der ersten pushschaltfläche zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e6514-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6514-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6514-120">Requirements</span></span>



| <span data-ttu-id="e6514-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6514-121">Requirement</span></span> | <span data-ttu-id="e6514-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e6514-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6514-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6514-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6514-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6514-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e6514-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6514-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6514-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6514-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6514-127">Header</span><span class="sxs-lookup"><span data-stu-id="e6514-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6514-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e6514-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6514-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6514-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6514-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e6514-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6514-131">**Defdlgproc**</span><span class="sxs-lookup"><span data-stu-id="e6514-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="e6514-132">**DM \_ getdefid**</span><span class="sxs-lookup"><span data-stu-id="e6514-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="e6514-133">**WM \_ getdlgcode**</span><span class="sxs-lookup"><span data-stu-id="e6514-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="e6514-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e6514-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6514-135">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="e6514-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="e6514-136">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e6514-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e6514-137">**BM- \_ SetStyle**</span><span class="sxs-lookup"><span data-stu-id="e6514-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="e6514-138">**EM \_ SetLimitText**</span><span class="sxs-lookup"><span data-stu-id="e6514-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 

