---
description: Legt die Schriftart fest, die ein Steuerelement beim Zeichnen von Text verwenden soll.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: WM_SETFONT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959810"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="f141a-103">WM- \_ setFont-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f141a-103">WM\_SETFONT message</span></span>

<span data-ttu-id="f141a-104">Legt die Schriftart fest, die ein Steuerelement beim Zeichnen von Text verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="f141a-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="f141a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f141a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f141a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f141a-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f141a-107">Ein Handle für die Schriftart (**hFont**).</span><span class="sxs-lookup"><span data-stu-id="f141a-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="f141a-108">Wenn dieser Parameter **null** ist, verwendet das Steuerelement die Standardsystem Schriftart, um Text zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="f141a-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="f141a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f141a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f141a-110">Das nieder wertige Wort von *LPARAM* gibt an, ob das Steuerelement sofort nach dem Festlegen der Schriftart neu gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f141a-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="f141a-111">Wenn dieser Parameter **true** ist, zeichnet sich das Steuerelement selbst neu auf.</span><span class="sxs-lookup"><span data-stu-id="f141a-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f141a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f141a-112">Return value</span></span>

<span data-ttu-id="f141a-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="f141a-113">Type: **LRESULT**</span></span>

<span data-ttu-id="f141a-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f141a-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f141a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f141a-115">Remarks</span></span>

<span data-ttu-id="f141a-116">Die **WM- \_ setFont** -Nachricht gilt für alle Steuerelemente, nicht nur für die in Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="f141a-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="f141a-117">Die beste Zeit für das Festlegen der Schriftart des Steuer Elements durch den Besitzer eines Dialogfeld-Steuer Elements ist, wenn die " [**WM \_ InitDialog**](../dlgbox/wm-initdialog.md) "-Meldung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f141a-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="f141a-118">Die Anwendung sollte die [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) -Funktion aufrufen, um die Schriftart zu löschen, wenn Sie nicht mehr benötigt wird. Dies ist beispielsweise der Fall, wenn das Steuerelement zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="f141a-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="f141a-119">Die Größe des Steuer Elements ändert sich nicht, wenn diese Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f141a-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="f141a-120">Um Clipping-Text zu vermeiden, der nicht in die Begrenzungen des Steuer Elements passt, sollte die Anwendung die Größe des Steuerelement Fensters korrigieren, bevor die Schriftart festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f141a-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="f141a-121">Wenn ein Dialogfeld den [DS- \_ setFont](../dlgbox/about-dialog-boxes.md) -Stil verwendet, um den Text in seinen Steuerelementen festzulegen, sendet das System die **WM- \_ setFont** -Nachricht an die Dialogfeld Prozedur, bevor die Steuerelemente erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f141a-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="f141a-122">Eine Anwendung kann ein Dialogfeld erstellen, das den DS-setFont-Stil enthält, indem Sie eine \_ der folgenden Funktionen aufruft:</span><span class="sxs-lookup"><span data-stu-id="f141a-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="f141a-123">**"Kreatedialogindirect"**</span><span class="sxs-lookup"><span data-stu-id="f141a-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="f141a-124">**"Kreatedialogindirectparam"**</span><span class="sxs-lookup"><span data-stu-id="f141a-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="f141a-125">**Dialogboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="f141a-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="f141a-126">**Dialogboxderedereparam**</span><span class="sxs-lookup"><span data-stu-id="f141a-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="f141a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f141a-127">Requirements</span></span>



| <span data-ttu-id="f141a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f141a-128">Requirement</span></span> | <span data-ttu-id="f141a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f141a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f141a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f141a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f141a-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f141a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f141a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f141a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f141a-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f141a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f141a-134">Header</span><span class="sxs-lookup"><span data-stu-id="f141a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f141a-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f141a-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f141a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f141a-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="f141a-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f141a-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f141a-138">**"Kreatedialogindirect"**</span><span class="sxs-lookup"><span data-stu-id="f141a-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="f141a-139">**"Kreatedialogindirectparam"**</span><span class="sxs-lookup"><span data-stu-id="f141a-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="f141a-140">**Dialogboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="f141a-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="f141a-141">**Dialogboxderedereparam**</span><span class="sxs-lookup"><span data-stu-id="f141a-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="f141a-142">**DLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="f141a-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="f141a-143">**Makelparam**</span><span class="sxs-lookup"><span data-stu-id="f141a-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="f141a-144">**WM- \_ getFont**</span><span class="sxs-lookup"><span data-stu-id="f141a-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="f141a-145">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="f141a-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="f141a-146">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f141a-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f141a-147">Windows</span><span class="sxs-lookup"><span data-stu-id="f141a-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="f141a-148">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="f141a-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f141a-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="f141a-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
