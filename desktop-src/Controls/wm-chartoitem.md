---
title: WM_CHARTOITEM Meldung (Winuser. h)
description: Wird von einem Listenfeld mit dem lbs- \_ wantkeyboardinput-Stil als Reaktion auf eine WM-char-Nachricht an seinen Besitzer gesendet \_ .
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Windows-Steuerelemente für WM_CHARTOITEM Meldung
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353918"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="602a4-104">WM- \_ chartoitem-Meldung</span><span class="sxs-lookup"><span data-stu-id="602a4-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="602a4-105">Wird von einem Listenfeld mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil als Reaktion auf eine [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht an seinen Besitzer gesendet.</span><span class="sxs-lookup"><span data-stu-id="602a4-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="602a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="602a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="602a4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="602a4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="602a4-108">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Zeichencode des Schlüssels an, den der Benutzer gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="602a4-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="602a4-109">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Element gibt die aktuelle Position der Einfügemarke an.</span><span class="sxs-lookup"><span data-stu-id="602a4-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="602a4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="602a4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="602a4-111">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="602a4-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="602a4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="602a4-112">Return value</span></span>

<span data-ttu-id="602a4-113">Der Rückgabewert gibt die Aktion an, die die Anwendung als Antwort auf die Nachricht ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="602a4-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="602a4-114">Der Rückgabewert-1 oder-2 gibt an, dass die Anwendung alle Aspekte der Elementauswahl behandelt hat und keine weitere Aktion im Listenfeld erfordert.</span><span class="sxs-lookup"><span data-stu-id="602a4-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="602a4-115">Ein Rückgabewert von 0 (null) oder größer gibt den NULL basierten Index eines Elements im Listenfeld an und gibt an, dass im Listenfeld die Standardaktion für den Tastatur Strich für das angegebene Element ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="602a4-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="602a4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="602a4-116">Remarks</span></span>

<span data-ttu-id="602a4-117">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="602a4-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="602a4-118">Nur vom Besitzer gezeichnete Listenfelder, die nicht den [**lbs \_ hasstrings**](list-box-styles.md) -Stil aufweisen, können diese Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="602a4-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="602a4-119">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="602a4-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="602a4-120">Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte *DWL- \_ msgresult* -Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="602a4-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="602a4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="602a4-121">Requirements</span></span>



| <span data-ttu-id="602a4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="602a4-122">Requirement</span></span> | <span data-ttu-id="602a4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="602a4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="602a4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="602a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="602a4-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="602a4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="602a4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="602a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="602a4-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="602a4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="602a4-128">Header</span><span class="sxs-lookup"><span data-stu-id="602a4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="602a4-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="602a4-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="602a4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="602a4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="602a4-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="602a4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="602a4-132">**WM \_ vkeytoitem**</span><span class="sxs-lookup"><span data-stu-id="602a4-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="602a4-133">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="602a4-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="602a4-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="602a4-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="602a4-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="602a4-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="602a4-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="602a4-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="602a4-137">**WM \_ -Zeichen**</span><span class="sxs-lookup"><span data-stu-id="602a4-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

