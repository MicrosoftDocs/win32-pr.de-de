---
title: WM_CTLCOLORDLG Meldung (Winuser. h)
description: Wird an ein Dialogfeld gesendet, bevor das System das Dialogfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das Dialogfeld die Text-und Hintergrundfarben mithilfe des angegebenen Kontext Handles für den Anzeigegerät festlegen.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Dialog Felder WM_CTLCOLORDLG Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740153"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="0b1b9-105">WM \_ ctlcolordlg-Meldung</span><span class="sxs-lookup"><span data-stu-id="0b1b9-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="0b1b9-106">Wird an ein Dialogfeld gesendet, bevor das System das Dialogfeld zeichnet.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="0b1b9-107">Wenn Sie auf diese Meldung reagieren, kann das Dialogfeld die Text-und Hintergrundfarben mithilfe des angegebenen Kontext Handles für den Anzeigegerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="0b1b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b1b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1b9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b1b9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1b9-110">Ein Handle für den Gerätekontext für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="0b1b9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b1b9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1b9-112">Ein Handle des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b1b9-113">Return value</span></span>

<span data-ttu-id="0b1b9-114">Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie ein Handle für einen Pinsel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="0b1b9-115">Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1b9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b1b9-116">Remarks</span></span>

<span data-ttu-id="0b1b9-117">Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standard Systemfarben für das Dialogfeld aus.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="0b1b9-118">Das System zerstört den zurückgegebenen Pinsel nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="0b1b9-119">Es ist Aufgabe der Anwendung, den Pinsel zu zerstören, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="0b1b9-120">Die " **WM \_ ctlcolordlg** "-Meldung wird nie zwischen Threads gesendet.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="0b1b9-121">Sie wird nur innerhalb eines Threads gesendet.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-121">It is sent only within one thread.</span></span>

<span data-ttu-id="0b1b9-122">Beachten Sie, dass die " **WM \_ ctlcolordlg** "-Nachricht an das Dialogfeld selbst gesendet wird. alle anderen \**WM \_ CtlColor \** _-Meldungen werden an den Besitzer des Steuer Elements gesendet.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="0b1b9-123">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein _ *int- \_ ptr*\* umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="0b1b9-124">Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="0b1b9-125">Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1b9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b1b9-126">Requirements</span></span>



| <span data-ttu-id="0b1b9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b1b9-127">Requirement</span></span> | <span data-ttu-id="0b1b9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0b1b9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1b9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b1b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1b9-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b1b9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0b1b9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b1b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1b9-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b1b9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b1b9-133">Header</span><span class="sxs-lookup"><span data-stu-id="0b1b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1b9-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0b1b9-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b1b9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b1b9-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b1b9-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b1b9-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="0b1b9-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="0b1b9-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0b1b9-140">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="0b1b9-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="0b1b9-141">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0b1b9-142">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="0b1b9-143">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="0b1b9-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

