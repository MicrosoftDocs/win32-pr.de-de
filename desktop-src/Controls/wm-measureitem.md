---
title: WM_MEASUREITEM Meldung (Winuser. h)
description: Wird an das Besitzer Fenster eines Kombinations Felds, eines Listen Felds, eines Listenansicht-Steuer Elements oder eines Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- Windows-Steuerelemente für WM_MEASUREITEM Meldung
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859046"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="aac37-104">WM \_ MeasureItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="aac37-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="aac37-105">Wird an das Besitzer Fenster eines Kombinations Felds, eines Listen Felds, eines Listenansicht-Steuer Elements oder eines Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="aac37-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="aac37-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="aac37-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aac37-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aac37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac37-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aac37-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aac37-109">Enthält den Wert des **ctlid** -Members der [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, auf die durch den *LPARAM* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="aac37-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="aac37-110">Dieser Wert identifiziert das Steuerelement, das die **WM \_ MeasureItem** -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="aac37-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="aac37-111">Wenn der Wert 0 (null) ist, wurde die Nachricht von einem Menü gesendet.</span><span class="sxs-lookup"><span data-stu-id="aac37-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="aac37-112">Wenn der Wert ungleich 0 (null) ist, wurde die Nachricht von einem Kombinations Feld oder einem Listenfeld gesendet.</span><span class="sxs-lookup"><span data-stu-id="aac37-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="aac37-113">Wenn der Wert ungleich 0 (null) ist und der Wert des **ItemID** -Members der **measureitemstruct** , auf den *LPARAM* zeigt, (uint) 1 ist, wurde die Nachricht von einem Kombinations Feld für die Bearbeitung gesendet.</span><span class="sxs-lookup"><span data-stu-id="aac37-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="aac37-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aac37-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aac37-115">Ein Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die die Dimensionen des vom Besitzer gezeichneten Steuer Elements oder Menü Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="aac37-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac37-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aac37-116">Return value</span></span>

<span data-ttu-id="aac37-117">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aac37-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac37-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aac37-118">Remarks</span></span>

<span data-ttu-id="aac37-119">Wenn das Besitzer Fenster die " **WM \_ MeasureItem** "-Meldung empfängt, füllt der Besitzer die [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur aus, auf die der *LPARAM* -Parameter der Nachricht verweist, und gibt zurück. Dadurch wird das System über die Abmessungen des Steuer Elements informiert.</span><span class="sxs-lookup"><span data-stu-id="aac37-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="aac37-120">Wenn ein Listenfeld oder Kombinations Feld mit der lbs- [**Besitzer \_ drawvariable**](list-box-styles.md) oder dem [**CBS \_**](combo-box-styles.md) -Besitzer der Eigenschaft "Besitzer" erstellt wird, wird diese Nachricht an den Besitzer für jedes Element im Steuerelement gesendet. andernfalls wird diese Nachricht einmal gesendet.</span><span class="sxs-lookup"><span data-stu-id="aac37-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="aac37-121">Das System sendet die **WM- \_ Datei "MeasureItem** " an das Fenster "Besitzer" der Kombinations Felder und Listenfelder, die mit der "besitzdrawfixed"-Formatvorlage erstellt werden, bevor die " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog)</span><span class="sxs-lookup"><span data-stu-id="aac37-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="aac37-122">Wenn der Besitzer diese Nachricht empfängt, hat das System die Höhe und Breite der im Steuerelement verwendeten Schriftart noch nicht bestimmt. Funktionsaufrufe und Berechnungen, die diese Werte erfordern, sollten in der Hauptfunktion der Anwendung oder der Bibliothek auftreten.</span><span class="sxs-lookup"><span data-stu-id="aac37-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac37-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aac37-123">Requirements</span></span>



| <span data-ttu-id="aac37-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aac37-124">Requirement</span></span> | <span data-ttu-id="aac37-125">Wert</span><span class="sxs-lookup"><span data-stu-id="aac37-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac37-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aac37-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aac37-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aac37-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aac37-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aac37-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aac37-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aac37-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aac37-130">Header</span><span class="sxs-lookup"><span data-stu-id="aac37-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac37-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="aac37-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac37-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac37-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="aac37-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="aac37-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aac37-134">**MEASUREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="aac37-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="aac37-135">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="aac37-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aac37-136">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="aac37-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

