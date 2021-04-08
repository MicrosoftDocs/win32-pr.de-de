---
title: LVN_DELETEALLITEMS Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass alle Elemente im Steuerelement gelöscht werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- Windows-Steuerelemente für LVN_DELETEALLITEMS Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957264"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="532d3-105">LVN \_ DeleteAllItems-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="532d3-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="532d3-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass alle Elemente im Steuerelement gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="532d3-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="532d3-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="532d3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="532d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="532d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="532d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="532d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="532d3-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="532d3-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="532d3-111">Das **iItem-Element** ist-1, und die anderen Member sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="532d3-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="532d3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="532d3-112">Return value</span></span>

<span data-ttu-id="532d3-113">Um nachfolgende [LVN \_ DeleteItem](lvn-deleteitem.md) -Benachrichtigungs Codes zu unterdrücken, geben Sie **true** zurück</span><span class="sxs-lookup"><span data-stu-id="532d3-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="532d3-114">Um nachfolgende [LVN \_ DeleteItem](lvn-deleteitem.md) -Benachrichtigungs Codes zu erhalten, geben Sie **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="532d3-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="532d3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="532d3-115">Remarks</span></span>

<span data-ttu-id="532d3-116">Ein Listenansicht-Steuerelement sendet den [**LVM- \_ DeleteAllItems**](lvm-deleteallitems.md) -Benachrichtigungs Code, wenn er zerstört wird oder die **LVM \_ DeleteAllItems** -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="532d3-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="532d3-117">Wenn " **LVM \_ DeleteAllItems** " nicht " **true**" zurückgibt, sendet das Steuerelement auch einen [LVN \_ DeleteItem](lvn-deleteitem.md) -Benachrichtigungs Code, wenn jedes Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="532d3-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="532d3-118">Wenn sich der " [**LVM \_ DeleteAllItems**](lvm-deleteallitems.md) "-Nachrichten Handler in einer Dialogfeld Prozedur befindet, geben Sie " **true** " aus der Dialogfeld Prozedur zurück, und verwenden Sie die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit DWL \_ msgresult, um den Nachrichten Rückgabewert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="532d3-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="532d3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="532d3-119">Requirements</span></span>



| <span data-ttu-id="532d3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="532d3-120">Requirement</span></span> | <span data-ttu-id="532d3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="532d3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="532d3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="532d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="532d3-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="532d3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="532d3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="532d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="532d3-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="532d3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="532d3-126">Header</span><span class="sxs-lookup"><span data-stu-id="532d3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="532d3-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="532d3-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

