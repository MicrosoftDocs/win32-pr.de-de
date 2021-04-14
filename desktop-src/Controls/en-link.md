---
title: EN_LINK Benachrichtigungs Code (RichEdit. h)
description: Ein RichEdit-Steuerelement sendet \_ beim empfangen verschiedener Nachrichten eine Eingabe-/Link-Benachrichtigung, z. b. wenn der Benutzer auf die Maus klickt oder wenn sich der Mauszeiger über dem Text befindet, der den CFE- \_ Link Effekt aufweist.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- Windows-Steuerelemente für EN_LINK Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478555"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="41a2f-104">EN \_ Link-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="41a2f-104">EN\_LINK notification code</span></span>

<span data-ttu-id="41a2f-105">Ein RichEdit-Steuerelement sendet \_ beim empfangen verschiedener Nachrichten eine Eingabe-/Link-Benachrichtigung, z. b. wenn der Benutzer auf die Maus klickt oder wenn sich der Mauszeiger über dem Text befindet, der den **CFE- \_ Link** Effekt aufweist.</span><span class="sxs-lookup"><span data-stu-id="41a2f-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="41a2f-106">Diese Benachrichtigung wird von einem fensterlosen Bearbeitungs Steuerelement mithilfe der [**itexthost:: txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) -Methode gesendet.</span><span class="sxs-lookup"><span data-stu-id="41a2f-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="41a2f-107">Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="41a2f-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="41a2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="41a2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a2f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41a2f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41a2f-110">Die Fenster-ID, die durch Aufrufen der [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) -Funktion mit dem GWL-ID-Wert abgerufen wird \_ .</span><span class="sxs-lookup"><span data-stu-id="41a2f-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="41a2f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41a2f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41a2f-112">Zeiger auf eine [**einlinkstruktur**](/windows/desktop/api/Richedit/ns-richedit-enlink) .</span><span class="sxs-lookup"><span data-stu-id="41a2f-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="41a2f-113">Die Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, Informationen über den Benachrichtigungs Code und eine [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur, die den Zeichenbereich angibt, der den **CFE- \_ Link** Effekt aufweist.</span><span class="sxs-lookup"><span data-stu-id="41a2f-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a2f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41a2f-114">Return value</span></span>

<span data-ttu-id="41a2f-115">Gibt NULL zurück, damit das Steuerelement mit der normalen Verarbeitung der Nachricht fortfahren kann.</span><span class="sxs-lookup"><span data-stu-id="41a2f-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="41a2f-116">Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement die Meldung</span><span class="sxs-lookup"><span data-stu-id="41a2f-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="41a2f-117">**Windows 8**: Rückgabe- **de- \_ Link \_ \_ standardmäßig** wird das Rich Edit-Steuerelement zum Ausführen der Standardaktion angewiesen.</span><span class="sxs-lookup"><span data-stu-id="41a2f-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="41a2f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41a2f-118">Remarks</span></span>

<span data-ttu-id="41a2f-119">Geben Sie das [**ENM- \_ linkflag**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht " [**EM \_ SetEventMask**](em-seteventmask.md) " gesendet wird, um die Verbindungs Benachrichtigungs Codes von **en \_** zu erhalten</span><span class="sxs-lookup"><span data-stu-id="41a2f-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="41a2f-120">Wenn der Link keinen Fokus hat, geben Sie zum Empfangen von **en- \_ Link** -Benachrichtigungs Codes das **SES \_ nofocuslinklotify** -Flag in der Maske an, die mit der [**EM \_ setEditStyle**](em-seteditstyle.md) -Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="41a2f-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="41a2f-121">Ein Rich-Edit-Steuerelement sendet beim Empfang der folgenden Meldungen die beim **empfangen der folgenden \_** Meldungen gesendeten **\_ Verbindungs** Benachrichtigungs Codes:</span><span class="sxs-lookup"><span data-stu-id="41a2f-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="41a2f-122">**WM \_ lbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="41a2f-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="41a2f-123">**WM \_ lbuttondown**</span><span class="sxs-lookup"><span data-stu-id="41a2f-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="41a2f-124">**WM- \_ lbuttonup**</span><span class="sxs-lookup"><span data-stu-id="41a2f-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="41a2f-125">**WM- \_ mouseelmove**</span><span class="sxs-lookup"><span data-stu-id="41a2f-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="41a2f-126">**WM- \_ rbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="41a2f-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="41a2f-127">**WM- \_ rbuttondown**</span><span class="sxs-lookup"><span data-stu-id="41a2f-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="41a2f-128">**WM- \_ rbuttonup**</span><span class="sxs-lookup"><span data-stu-id="41a2f-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="41a2f-129">**WM- \_ SetCursor**</span><span class="sxs-lookup"><span data-stu-id="41a2f-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="41a2f-130">Der **CFE- \_ Link** Effekt identifiziert in der Regel einen Textbereich, der eine URL enthält.</span><span class="sxs-lookup"><span data-stu-id="41a2f-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="41a2f-131">Anwendungen können den e- \_ Link-Benachrichtigungs Code verarbeiten, indem Sie den Mauszeiger ändern, wenn er sich über der URL befindet, oder indem Sie einen Browser starten, um den von der URL identifizierten Speicherort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="41a2f-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="41a2f-132">Wenn Sie die [**EM \_ autourldetect**](em-autourldetect.md) -Nachricht senden, um die automatische URL-Erkennung zu aktivieren, legt das Rich Edit-Steuerelement automatisch den **CFE- \_ Link** Effekt für geänderten Text fest, der als URL identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="41a2f-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a2f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41a2f-133">Requirements</span></span>



| <span data-ttu-id="41a2f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41a2f-134">Requirement</span></span> | <span data-ttu-id="41a2f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="41a2f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41a2f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41a2f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="41a2f-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41a2f-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41a2f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41a2f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="41a2f-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41a2f-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41a2f-140">Header</span><span class="sxs-lookup"><span data-stu-id="41a2f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a2f-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a2f-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41a2f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a2f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a2f-143">**Zeichenbereich**</span><span class="sxs-lookup"><span data-stu-id="41a2f-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="41a2f-144">**EM \_ autourldetect**</span><span class="sxs-lookup"><span data-stu-id="41a2f-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="41a2f-145">**Verknüpfen**</span><span class="sxs-lookup"><span data-stu-id="41a2f-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="41a2f-146">**ITextRange2:: tarturl**</span><span class="sxs-lookup"><span data-stu-id="41a2f-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="41a2f-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="41a2f-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

