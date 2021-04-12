---
title: WM_VKEYTOITEM Meldung (Winuser. h)
description: Wird von einem Listenfeld mit dem lbs- \_ wantkeyboardinput-Stil an seinen Besitzer als Antwort auf eine WM- \_ KeyDown-Nachricht gesendet.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Windows-Steuerelemente für WM_VKEYTOITEM Meldung
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "104351729"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="0e980-104">WM- \_ vkeytoitem-Meldung</span><span class="sxs-lookup"><span data-stu-id="0e980-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="0e980-105">Wird von einem Listenfeld mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil an seinen Besitzer als Antwort auf eine [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="0e980-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0e980-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e980-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e980-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e980-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e980-108">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Code des virtuellen Schlüssels der vom Benutzer gedrückten Taste an.</span><span class="sxs-lookup"><span data-stu-id="0e980-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="0e980-109">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Element gibt die aktuelle Position der Einfügemarke an.</span><span class="sxs-lookup"><span data-stu-id="0e980-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="0e980-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e980-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e980-111">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="0e980-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e980-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e980-112">Return value</span></span>

<span data-ttu-id="0e980-113">Der Rückgabewert gibt die Aktion an, die die Anwendung als Antwort auf die Nachricht ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="0e980-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="0e980-114">Der Rückgabewert-2 gibt an, dass die Anwendung alle Aspekte der Elementauswahl behandelt hat und keine weitere Aktion im Listenfeld erfordert.</span><span class="sxs-lookup"><span data-stu-id="0e980-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="0e980-115">(Siehe Hinweise.) Der Rückgabewert-1 gibt an, dass das Listenfeld die Standardaktion als Reaktion auf den Tastatur Strich ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="0e980-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="0e980-116">Ein Rückgabewert von 0 (null) oder größer gibt den Index eines Elements im Listenfeld an und gibt an, dass im Listenfeld die Standardaktion für den Tastatur Strich für das angegebene Element ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e980-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e980-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e980-117">Remarks</span></span>

<span data-ttu-id="0e980-118">Der Rückgabewert-2 ist nur für Schlüssel gültig, die vom Listenfeld-Steuerelement nicht in Zeichen übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0e980-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="0e980-119">Wenn die [**WM- \_ keydownnachricht**](/windows/desktop/inputdev/wm-keydown) in eine [**WM \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht übersetzt wird und die Anwendung die als Ergebnis des Tastendruck generierte **WM \_ vkeytoitem** -Nachricht verarbeitet, ignoriert das Listenfeld den Rückgabewert und übernimmt die Standard Verarbeitung für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0e980-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="0e980-120">**WM \_ KeyDown** -Nachrichten, die von Schlüsseln wie "VK \_ up", "VK \_ down", "VK Next" und " \_ VK Previous" generiert werden, \_ werden nicht in " **WM \_ char**</span><span class="sxs-lookup"><span data-stu-id="0e980-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="0e980-121">In solchen Fällen wird durch das Abfangen der **WM \_ vkeytoitem** -Nachricht und die Rückgabe von-2 verhindert, dass das Listenfeld die Standard Verarbeitung für diesen Schlüssel vornimmt.</span><span class="sxs-lookup"><span data-stu-id="0e980-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="0e980-122">Zum Abfangen von Schlüsseln, die eine char-Nachricht generieren und eine spezielle Verarbeitung durchführen, muss die Anwendung das Listenfeld unterteilen, sowohl die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -als auch die [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht abfangen und die Nachrichten entsprechend in der Unterklassen Prozedur verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0e980-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="0e980-123">Die vorangehenden Hinweise gelten für reguläre Listenfelder, die mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0e980-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="0e980-124">Wenn das Listenfeld vom Besitzer gezeichnet wird, muss die Anwendung die " [**WM \_ chartoitem**](wm-chartoitem.md) "-Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0e980-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="0e980-125">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="0e980-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="0e980-126">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0e980-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="0e980-127">Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0e980-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e980-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e980-128">Requirements</span></span>



| <span data-ttu-id="0e980-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e980-129">Requirement</span></span> | <span data-ttu-id="0e980-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0e980-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e980-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e980-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0e980-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e980-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0e980-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e980-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0e980-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e980-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e980-135">Header</span><span class="sxs-lookup"><span data-stu-id="0e980-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e980-136"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0e980-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e980-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e980-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e980-138">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0e980-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e980-139">**WM- \_ Diagramm**</span><span class="sxs-lookup"><span data-stu-id="0e980-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="0e980-140">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="0e980-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0e980-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e980-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0e980-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e980-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0e980-143">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="0e980-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

