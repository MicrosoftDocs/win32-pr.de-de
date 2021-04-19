---
title: WM_COPY Meldung (Winuser. h)
description: Eine Anwendung sendet die WM- \_ Kopier Nachricht an ein Bearbeitungs Steuerelement oder ein Kombinations Feld, um die aktuelle Auswahl im CF-Text Format in die Zwischenablage zu kopieren \_ .
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106363895"
---
# <a name="wm_copy-message"></a><span data-ttu-id="04144-104">WM- \_ Kopier Nachricht</span><span class="sxs-lookup"><span data-stu-id="04144-104">WM\_COPY message</span></span>

<span data-ttu-id="04144-105">Eine Anwendung sendet die **WM- \_ Kopier** Nachricht an ein Bearbeitungs Steuerelement oder ein Kombinations Feld, um die aktuelle Auswahl im [**CF- \_ Text**](standard-clipboard-formats.md) Format in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="04144-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="04144-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04144-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04144-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04144-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04144-108">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="04144-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="04144-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04144-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04144-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="04144-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04144-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04144-111">Return value</span></span>

<span data-ttu-id="04144-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="04144-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="04144-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04144-113">Remarks</span></span>

<span data-ttu-id="04144-114">Beim Senden an ein Kombinations Feld wird die **WM- \_ Kopier** Nachricht durch das Bearbeitungs Steuerelement behandelt.</span><span class="sxs-lookup"><span data-stu-id="04144-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="04144-115">Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="04144-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="04144-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04144-116">Requirements</span></span>



| <span data-ttu-id="04144-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04144-117">Requirement</span></span> | <span data-ttu-id="04144-118">Wert</span><span class="sxs-lookup"><span data-stu-id="04144-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04144-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04144-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04144-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04144-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="04144-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04144-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04144-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04144-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04144-123">Header</span><span class="sxs-lookup"><span data-stu-id="04144-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04144-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="04144-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04144-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04144-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="04144-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="04144-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04144-127">**WM \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="04144-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="04144-128">**WM \_ Ausschneiden**</span><span class="sxs-lookup"><span data-stu-id="04144-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="04144-129">**WM \_ Einfügen**</span><span class="sxs-lookup"><span data-stu-id="04144-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="04144-130">**WM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="04144-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="04144-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="04144-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="04144-132">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="04144-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

