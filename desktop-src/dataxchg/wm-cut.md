---
title: WM_CUT Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM \_ -Ausschneide Nachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um die aktuelle Auswahl (sofern vorhanden) im Bearbeitungs Steuerelement zu löschen (Ausschneiden) und den gelöschten Text im CF-Textformat in die Zwischenablage zu kopieren \_ .
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338332"
---
# <a name="wm_cut-message"></a><span data-ttu-id="0248d-104">WM- \_ Ausschneide Nachricht</span><span class="sxs-lookup"><span data-stu-id="0248d-104">WM\_CUT message</span></span>

<span data-ttu-id="0248d-105">Eine Anwendung sendet eine **WM- \_ Ausschneide** Nachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um die aktuelle Auswahl (sofern vorhanden) im Bearbeitungs Steuerelement zu löschen (Ausschneiden) und den gelöschten Text im [**CF- \_ Text**](standard-clipboard-formats.md) Format in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0248d-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="0248d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0248d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0248d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0248d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0248d-108">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0248d-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0248d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0248d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0248d-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0248d-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0248d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0248d-111">Return value</span></span>

<span data-ttu-id="0248d-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0248d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0248d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0248d-113">Remarks</span></span>

<span data-ttu-id="0248d-114">Der von der WM- **\_ Ausschneide** Nachricht ausgeführte Löschvorgang kann rückgängig gemacht werden, indem das Bearbeitungs Steuerelement eine [**EM- \_ Rückgängig**](../controls/em-undo.md) -Meldung</span><span class="sxs-lookup"><span data-stu-id="0248d-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="0248d-115">Um die aktuelle Auswahl zu löschen, ohne den gelöschten Text in der Zwischenablage zu platzieren, verwenden Sie die unverschlüsselte [**WM \_**](wm-clear.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0248d-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="0248d-116">Beim Senden an ein Kombinations Feld wird die **WM- \_ Ausschneide** Nachricht durch das Bearbeitungs Steuerelement behandelt.</span><span class="sxs-lookup"><span data-stu-id="0248d-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="0248d-117">Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0248d-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0248d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0248d-118">Requirements</span></span>



| <span data-ttu-id="0248d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0248d-119">Requirement</span></span> | <span data-ttu-id="0248d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0248d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0248d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0248d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0248d-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0248d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0248d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0248d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0248d-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0248d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0248d-125">Header</span><span class="sxs-lookup"><span data-stu-id="0248d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0248d-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0248d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0248d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0248d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0248d-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0248d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0248d-129">**WM \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="0248d-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="0248d-130">**WM- \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="0248d-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="0248d-131">**WM \_ Einfügen**</span><span class="sxs-lookup"><span data-stu-id="0248d-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="0248d-132">**WM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="0248d-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="0248d-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0248d-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0248d-134">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="0248d-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="0248d-135">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="0248d-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0248d-136">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="0248d-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

