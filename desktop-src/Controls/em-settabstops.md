---
title: EM_SETTABSTOPS Meldung (Winuser. h)
description: Die \_ gesettabstopps-Meldung legt die Tabstopps in einem mehrzeiligen Bearbeitungs Steuerelement fest.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Windows-Steuerelemente für EM_SETTABSTOPS Meldung
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104211"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="c305f-104">EM \_ settabstopps-Meldung</span><span class="sxs-lookup"><span data-stu-id="c305f-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="c305f-105">Die **\_ gesettabstopps** -Meldung legt die Tabstopps in einem mehrzeiligen Bearbeitungs Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="c305f-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="c305f-106">Wenn Text in das-Steuerelement kopiert wird, bewirkt jedes Tabulator Zeichen im Text, dass der Bereich bis zum nächsten Tabstopp Zeichen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c305f-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="c305f-107">Diese Meldung wird nur von mehrzeiligen Bearbeitungs Steuerelementen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c305f-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="c305f-108">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="c305f-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c305f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c305f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c305f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c305f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c305f-111">Die Anzahl der Tabstopps, die im Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c305f-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="c305f-112">Wenn dieser Parameter NULL ist, wird der *LPARAM* -Parameter ignoriert, und Standard Tabstopps werden bei jeder 32-Dialogfeld Vorlagen-Einheit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c305f-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="c305f-113">Wenn dieser Parameter 1 ist, werden Tabstopps bei allen *n* Dialogfeld Vorlagen Einheiten festgelegt, wobei *n* der Abstand ist, auf den der *LPARAM* -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="c305f-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="c305f-114">Wenn dieser Parameter größer als 1 ist, ist *LPARAM* ein Zeiger auf ein Array von Tabstopps.</span><span class="sxs-lookup"><span data-stu-id="c305f-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="c305f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c305f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c305f-116">Ein Zeiger auf ein Array von ganzen Zahlen ohne Vorzeichen, das die Tabstopps in Dialogfeld Vorlagen Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="c305f-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="c305f-117">Wenn der *wParam* -Parameter 1 ist, ist dieser Parameter ein Zeiger auf eine ganze Zahl ohne Vorzeichen, die den Abstand zwischen allen Tabstopps in Dialogfeld Vorlagen Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="c305f-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c305f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c305f-118">Return value</span></span>

<span data-ttu-id="c305f-119">Wenn alle Registerkarten festgelegt sind, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="c305f-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="c305f-120">Wenn nicht alle Registerkarten festgelegt sind, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="c305f-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c305f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c305f-121">Remarks</span></span>

<span data-ttu-id="c305f-122">Die Meldung " **EM \_ settabstopps** " zeichnet das Bearbeitungs Steuerelement Fenster nicht automatisch neu auf.</span><span class="sxs-lookup"><span data-stu-id="c305f-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="c305f-123">Wenn die Anwendung die Tabstopps für Text ändert, der sich bereits im Bearbeitungs Steuerelement befindet, sollte Sie die [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) -Funktion aufrufen, um das Bearbeitungs Steuerelement Fenster neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c305f-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="c305f-124">Die im Array angegebenen Werte befinden sich in Dialogfeld Vorlagen Einheiten, die die geräteunabhängigen Einheiten sind, die in Dialogfeld Vorlagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c305f-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="c305f-125">Verwenden Sie die [**mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) -Funktion, um Messungen von Dialogfeld Vorlagen-Einheiten in Bildschirm Einheiten (Pixel) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c305f-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="c305f-126">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 3,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c305f-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="c305f-127">Ein Rich-Edit-Steuerelement kann die maximale Anzahl von Tabstopps aufweisen, die durch maximale \_ \_ Tabstopps angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c305f-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="c305f-128">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="c305f-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c305f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c305f-129">Requirements</span></span>



| <span data-ttu-id="c305f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c305f-130">Requirement</span></span> | <span data-ttu-id="c305f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c305f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c305f-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c305f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c305f-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c305f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c305f-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c305f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c305f-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c305f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c305f-136">Header</span><span class="sxs-lookup"><span data-stu-id="c305f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c305f-137"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c305f-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c305f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c305f-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="c305f-139">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c305f-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c305f-140">**Invalidateruieren**</span><span class="sxs-lookup"><span data-stu-id="c305f-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="c305f-141">**Mapdialogrect**</span><span class="sxs-lookup"><span data-stu-id="c305f-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

