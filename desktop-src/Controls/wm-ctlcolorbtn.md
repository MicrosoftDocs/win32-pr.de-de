---
title: WM_CTLCOLORBTN Meldung (Winuser. h)
description: Die "WM \_ ctlcolorbtn"-Meldung wird vor dem Zeichnen der Schaltfläche an das übergeordnete Fenster einer Schaltfläche gesendet. Das übergeordnete Fenster kann die Text-und Hintergrundfarben der Schaltfläche ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Nachricht verarbeitet.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- Windows-Steuerelemente für WM_CTLCOLORBTN Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949407"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="929b7-106">WM \_ ctlcolorbtn-Nachricht</span><span class="sxs-lookup"><span data-stu-id="929b7-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="929b7-107">Die " **WM \_ ctlcolorbtn** "-Meldung wird vor dem Zeichnen der Schaltfläche an das übergeordnete Fenster einer Schaltfläche gesendet.</span><span class="sxs-lookup"><span data-stu-id="929b7-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="929b7-108">Das übergeordnete Fenster kann die Text-und Hintergrundfarben der Schaltfläche ändern.</span><span class="sxs-lookup"><span data-stu-id="929b7-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="929b7-109">Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="929b7-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="929b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="929b7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="929b7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="929b7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="929b7-112">Ein **hdc** , der das Handle für den Anzeige Kontext der Schaltfläche angibt.</span><span class="sxs-lookup"><span data-stu-id="929b7-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="929b7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="929b7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="929b7-114">Ein **HWND** , das das Handle für die Schaltfläche angibt.</span><span class="sxs-lookup"><span data-stu-id="929b7-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="929b7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="929b7-115">Return value</span></span>

<span data-ttu-id="929b7-116">Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie ein Handle für einen Pinsel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="929b7-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="929b7-117">Das System verwendet den Pinsel zum Zeichnen des Hintergrunds der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="929b7-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="929b7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="929b7-118">Remarks</span></span>

<span data-ttu-id="929b7-119">Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben.</span><span class="sxs-lookup"><span data-stu-id="929b7-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="929b7-120">Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="929b7-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="929b7-121">Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für die Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="929b7-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="929b7-122">Schaltflächen mit den Formen " [**b \_ Push Button**](button-styles.md)", " [**b \_ DEFPUSHBUTTON**](button-styles.md)" oder "SB [**\_ Push like**](button-styles.md) " verwenden den zurückgegebenen Pinsel nicht.</span><span class="sxs-lookup"><span data-stu-id="929b7-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="929b7-123">Schaltflächen mit diesen Stilen werden immer mit den Standardsystem Farben gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="929b7-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="929b7-124">Das Zeichnen von Push-Schaltflächen erfordert mehrere verschiedene Pinsel Gesichter, Hervorhebung und Schatten, aber die **WM \_ ctlcolorbtn** -Meldung ermöglicht nur die Rückgabe eines einzelnen Pinsels.</span><span class="sxs-lookup"><span data-stu-id="929b7-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="929b7-125">Verwenden Sie zum Bereitstellen einer benutzerdefinierten Darstellung für pushschaltflächen eine vom Besitzer gezeichnete Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="929b7-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="929b7-126">Weitere Informationen finden Sie unter [Erstellen von Owner-Drawn](user-controls-intro.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="929b7-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="929b7-127">Die " **WM \_ ctlcolorbtn** "-Nachricht wird nie zwischen Threads gesendet.</span><span class="sxs-lookup"><span data-stu-id="929b7-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="929b7-128">Sie wird nur innerhalb eines Threads gesendet.</span><span class="sxs-lookup"><span data-stu-id="929b7-128">It is sent only within one thread.</span></span>

<span data-ttu-id="929b7-129">Die Textfarbe eines Kontrollkästchens oder Options Felds gilt für das Feld bzw. die Schaltfläche, das Häkchen und den Text.</span><span class="sxs-lookup"><span data-stu-id="929b7-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="929b7-130">Das Fokus Rechteck für diese Schaltflächen bleibt die Standardfarbe des Systems (normalerweise schwarz).</span><span class="sxs-lookup"><span data-stu-id="929b7-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="929b7-131">Die Textfarbe eines Gruppen Felds bezieht sich auf den Text, jedoch nicht auf die Zeile, in der das Feld definiert ist.</span><span class="sxs-lookup"><span data-stu-id="929b7-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="929b7-132">Die Textfarbe einer Schaltfläche für den Push gilt nur für das Fokus Rechteck. Dies hat keine Auswirkung auf die Farbe des Texts.</span><span class="sxs-lookup"><span data-stu-id="929b7-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="929b7-133">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="929b7-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="929b7-134">Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="929b7-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="929b7-135">Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="929b7-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="929b7-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="929b7-136">Requirements</span></span>



| <span data-ttu-id="929b7-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="929b7-137">Requirement</span></span> | <span data-ttu-id="929b7-138">Wert</span><span class="sxs-lookup"><span data-stu-id="929b7-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="929b7-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="929b7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="929b7-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="929b7-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="929b7-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="929b7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="929b7-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="929b7-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="929b7-143">Header</span><span class="sxs-lookup"><span data-stu-id="929b7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="929b7-144"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="929b7-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="929b7-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="929b7-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="929b7-146">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="929b7-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="929b7-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="929b7-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="929b7-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="929b7-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

