---
title: WM_INITDIALOG Meldung (Winuser. h)
description: Wird an die Dialogfeld Prozedur gesendet, unmittelbar bevor ein Dialogfeld angezeigt wird. Dialog Feld Prozeduren verwenden diese Meldung in der Regel, um Steuerelemente zu initialisieren und alle anderen Initialisierungs Aufgaben auszuführen, die sich auf die Darstellung des Dialog Felds auswirken.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Dialog Felder WM_INITDIALOG Meldung
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346737"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="86318-105">WM- \_ InitDialog-Meldung</span><span class="sxs-lookup"><span data-stu-id="86318-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="86318-106">Wird an die Dialogfeld Prozedur gesendet, unmittelbar bevor ein Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="86318-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="86318-107">Dialog Feld Prozeduren verwenden diese Meldung in der Regel, um Steuerelemente zu initialisieren und alle anderen Initialisierungs Aufgaben auszuführen, die sich auf die Darstellung des Dialog Felds auswirken.</span><span class="sxs-lookup"><span data-stu-id="86318-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="86318-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="86318-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86318-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86318-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86318-110">Ein Handle für das-Steuerelement, das den Standardtastatur Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="86318-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="86318-111">Das System weist den Standardtastatur Fokus nur zu, wenn die Dialogfeld Prozedur **true** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="86318-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="86318-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86318-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86318-113">Zusätzliche Initialisierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="86318-113">Additional initialization data.</span></span> <span data-ttu-id="86318-114">Diese Daten werden als lParam-Parameter in einem aufgerufen, der zum Erstellen des Dialog Felds verwendet wird [](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) , als *LPARAM* - [](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)Parameter in einem aufzurufenden [](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)Befehl [**an die Funktion**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)"" von "".</span><span class="sxs-lookup"><span data-stu-id="86318-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="86318-115">Bei Eigenschaften Blättern ist dieser Parameter ein Zeiger auf die [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur, die zum Erstellen der Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86318-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="86318-116">Dieser Parameter ist 0 (null), wenn eine andere Dialogfeld-Erstellungs Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86318-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86318-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86318-117">Return value</span></span>

<span data-ttu-id="86318-118">Die Dialogfeld Prozedur sollte **true** zurückgeben, um das System anzuweisen, den Tastaturfokus auf das von *wParam* angegebene Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="86318-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="86318-119">Andernfalls sollte **false** zurückgegeben werden, um zu verhindern, dass das System den Standardtastatur Fokus festlegt.</span><span class="sxs-lookup"><span data-stu-id="86318-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="86318-120">Die Dialogfeld Prozedur sollte den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="86318-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="86318-121">Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="86318-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="86318-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86318-122">Remarks</span></span>

<span data-ttu-id="86318-123">Das Steuerelement, das den Standardtastatur Fokus erhält, ist immer das erste Steuerelement im Dialogfeld, das sichtbar und nicht deaktiviert ist und das die **WS \_ Tabstopps** -Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="86318-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="86318-124">Wenn die Dialogfeld Prozedur **true** zurückgibt, prüft das System das Steuerelement, um sicherzustellen, dass es von der Prozedur nicht deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="86318-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="86318-125">Wenn Sie deaktiviert wurde, legt das System den Tastaturfokus auf das nächste Steuerelement fest, das sichtbar und nicht deaktiviert ist und über das **WS \_ Tabstopps** verfügt.</span><span class="sxs-lookup"><span data-stu-id="86318-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="86318-126">Eine Anwendung kann nur dann **false** zurückgeben, wenn Sie den Tastaturfokus auf eines der Steuerelemente des Dialog Felds festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="86318-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="86318-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86318-127">Requirements</span></span>



| <span data-ttu-id="86318-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86318-128">Requirement</span></span> | <span data-ttu-id="86318-129">Wert</span><span class="sxs-lookup"><span data-stu-id="86318-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86318-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86318-130">Minimum supported client</span></span><br/> | <span data-ttu-id="86318-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86318-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="86318-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86318-132">Minimum supported server</span></span><br/> | <span data-ttu-id="86318-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86318-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86318-134">Header</span><span class="sxs-lookup"><span data-stu-id="86318-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="86318-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="86318-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86318-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86318-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="86318-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="86318-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86318-138">**"Kreatedialogindirectparam"**</span><span class="sxs-lookup"><span data-stu-id="86318-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="86318-139">**"Kreatedialogparam"**</span><span class="sxs-lookup"><span data-stu-id="86318-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="86318-140">**Dialogboxderedereparam**</span><span class="sxs-lookup"><span data-stu-id="86318-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="86318-141">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="86318-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="86318-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="86318-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="86318-143">**Licher**</span><span class="sxs-lookup"><span data-stu-id="86318-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="86318-144">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="86318-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="86318-145">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="86318-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="86318-146">**PROPSHEETPAGE**</span><span class="sxs-lookup"><span data-stu-id="86318-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

