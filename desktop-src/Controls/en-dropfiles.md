---
title: EN_DROPFILES Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer versucht, Dateien im Steuerelement abzulegen. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung, wenn er die WM- \_ dropfiles-Nachricht empfängt.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- Windows-Steuerelemente für EN_DROPFILES Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475393"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="2f9ea-105">EN \_ dropfiles-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2f9ea-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="2f9ea-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer versucht, Dateien im Steuerelement abzulegen.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="2f9ea-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung, wenn er die [**WM- \_ dropfiles**](/windows/desktop/shell/wm-dropfiles) -Nachricht empfängt. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="2f9ea-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2f9ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f9ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f9ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f9ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f9ea-110">Eine [**endropfiles**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) -Struktur, die gelöschte Dateiinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f9ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f9ea-111">Return value</span></span>

<span data-ttu-id="2f9ea-112">Gibt einen Wert ungleich 0 (null) zurück, um den Löschvorgang zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="2f9ea-113">Gibt NULL zurück, um den Drop-Vorgang zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f9ea-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f9ea-114">Remarks</span></span>

<span data-ttu-id="2f9ea-115">Damit ein Rich-Edit-Steuerelement die [**WM- \_ dropfiles**](/windows/desktop/shell/wm-dropfiles) -Meldungen empfängt, muss das übergeordnete Fenster das Steuerelement als Ablage Ziel mithilfe der [**dragaccept-files**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) -Funktion registrieren.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="2f9ea-116">Das Steuerelement registriert sich nicht selbst.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-116">The control does not register itself.</span></span>

<span data-ttu-id="2f9ea-117">Geben Sie zum Empfangen von en \_ dropfiles-Benachrichtigungs Codes [**ENM \_ dropfiles**](rich-edit-control-event-mask-flags.md) in der mit der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) gesendeten Maske an.</span><span class="sxs-lookup"><span data-stu-id="2f9ea-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f9ea-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f9ea-118">Requirements</span></span>



| <span data-ttu-id="2f9ea-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f9ea-119">Requirement</span></span> | <span data-ttu-id="2f9ea-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2f9ea-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9ea-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f9ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9ea-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f9ea-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f9ea-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f9ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9ea-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f9ea-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f9ea-125">Header</span><span class="sxs-lookup"><span data-stu-id="2f9ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f9ea-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f9ea-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f9ea-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f9ea-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f9ea-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2f9ea-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f9ea-129">**Endropfiles**</span><span class="sxs-lookup"><span data-stu-id="2f9ea-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

