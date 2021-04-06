---
description: Legt den Text eines Fensters fest.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: WM_SETTEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759493"
---
# <a name="wm_settext-message"></a><span data-ttu-id="881c4-103">WM- \_ SetText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="881c4-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="881c4-104">Legt den Text eines Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="881c4-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="881c4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="881c4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="881c4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="881c4-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="881c4-107">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="881c4-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="881c4-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="881c4-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="881c4-109">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Fenster Text ist.</span><span class="sxs-lookup"><span data-stu-id="881c4-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="881c4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="881c4-110">Return value</span></span>

<span data-ttu-id="881c4-111">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="881c4-111">Type: **LRESULT**</span></span>

<span data-ttu-id="881c4-112">Der Rückgabewert ist **true** , wenn der Text festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="881c4-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="881c4-113">Es ist **false** (bei einem Bearbeitungs Steuerelement), **lb- \_ errspace** (für ein Listenfeld) oder **CB \_ errspace** (für ein Kombinations Feld), wenn nicht genügend Speicherplatz zum Festlegen des Texts im Bearbeitungs Steuerelement verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="881c4-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="881c4-114">Es ist **CB \_ Err** , wenn diese Nachricht an ein Kombinations Feld ohne Bearbeitungs Steuerelement gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="881c4-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="881c4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="881c4-115">Remarks</span></span>

<span data-ttu-id="881c4-116">Mit der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion wird der Fenster Text festgelegt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="881c4-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="881c4-117">Bei einem Bearbeitungs Steuerelement ist der Text der Inhalt des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="881c4-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="881c4-118">Bei einem Kombinations Feld ist der Text der Inhalt des Bearbeitungs Steuer Elements im Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="881c4-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="881c4-119">Für eine Schaltfläche ist der Text der Schaltflächen Name.</span><span class="sxs-lookup"><span data-stu-id="881c4-119">For a button, the text is the button name.</span></span> <span data-ttu-id="881c4-120">Bei anderen Fenstern ist der Text der Fenstertitel.</span><span class="sxs-lookup"><span data-stu-id="881c4-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="881c4-121">Mit dieser Meldung wird die aktuelle Auswahl im Listenfeld eines Kombinations Felds nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="881c4-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="881c4-122">Eine Anwendung sollte die [**CB- \_ SelectString**](../controls/cb-selectstring.md) -Nachricht verwenden, um das Element in einem Listenfeld auszuwählen, das mit dem Text im Bearbeitungs Steuerelement übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="881c4-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="881c4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="881c4-123">Requirements</span></span>



| <span data-ttu-id="881c4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="881c4-124">Requirement</span></span> | <span data-ttu-id="881c4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="881c4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881c4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="881c4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="881c4-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="881c4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="881c4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="881c4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="881c4-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="881c4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="881c4-130">Header</span><span class="sxs-lookup"><span data-stu-id="881c4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="881c4-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="881c4-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="881c4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="881c4-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="881c4-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="881c4-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="881c4-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="881c4-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="881c4-135">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="881c4-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="881c4-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="881c4-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="881c4-137">Windows</span><span class="sxs-lookup"><span data-stu-id="881c4-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="881c4-138">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="881c4-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="881c4-139">**CB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="881c4-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
