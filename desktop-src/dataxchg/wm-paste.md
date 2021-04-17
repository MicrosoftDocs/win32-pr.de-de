---
title: WM_PASTE Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM- \_ einfügenachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um den aktuellen Inhalt der Zwischenablage an der aktuellen Position der Einfügemarke in das Bearbeitungs Steuerelement zu kopieren. Daten werden nur eingefügt, wenn die Zwischenablage Daten im CF- \_ Text Format enthält.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392130"
---
# <a name="wm_paste-message"></a><span data-ttu-id="8bf5f-105">WM- \_ Einfüge Nachricht</span><span class="sxs-lookup"><span data-stu-id="8bf5f-105">WM\_PASTE message</span></span>

<span data-ttu-id="8bf5f-106">Eine Anwendung sendet eine **WM \_** -einfügenachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um den aktuellen Inhalt der Zwischenablage an der aktuellen Position der Einfügemarke in das Bearbeitungs Steuerelement zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="8bf5f-107">Daten werden nur eingefügt, wenn die Zwischenablage Daten im [**CF- \_ Text**](standard-clipboard-formats.md) Format enthält.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="8bf5f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bf5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bf5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf5f-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8bf5f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bf5f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf5f-112">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf5f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bf5f-113">Return value</span></span>

<span data-ttu-id="8bf5f-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf5f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bf5f-115">Remarks</span></span>

<span data-ttu-id="8bf5f-116">Beim Senden an ein Kombinations Feld wird die **WM- \_ Einfüge** Nachricht durch das Bearbeitungs Steuerelement behandelt.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="8bf5f-117">Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bf5f-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf5f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bf5f-118">Requirements</span></span>



| <span data-ttu-id="8bf5f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bf5f-119">Requirement</span></span> | <span data-ttu-id="8bf5f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8bf5f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf5f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bf5f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf5f-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bf5f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8bf5f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bf5f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf5f-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bf5f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8bf5f-125">Header</span><span class="sxs-lookup"><span data-stu-id="8bf5f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf5f-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf5f-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf5f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bf5f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8bf5f-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8bf5f-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8bf5f-129">**WM \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="8bf5f-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="8bf5f-130">**WM- \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="8bf5f-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="8bf5f-131">**WM \_ Ausschneiden**</span><span class="sxs-lookup"><span data-stu-id="8bf5f-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="8bf5f-132">**WM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="8bf5f-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="8bf5f-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8bf5f-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8bf5f-134">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="8bf5f-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

