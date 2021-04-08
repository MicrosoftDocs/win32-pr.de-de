---
description: Bestimmt die Länge des Texts, der einem Fenster zugeordnet ist, in Zeichen.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: WM_GETTEXTLENGTH Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960171"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="c4661-103">WM \_ getTextLength-Meldung</span><span class="sxs-lookup"><span data-stu-id="c4661-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="c4661-104">Bestimmt die Länge des Texts, der einem Fenster zugeordnet ist, in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c4661-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="c4661-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4661-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4661-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4661-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4661-107">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c4661-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4661-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4661-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4661-109">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c4661-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4661-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4661-110">Return value</span></span>

<span data-ttu-id="c4661-111">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4661-111">Type: **LRESULT**</span></span>

<span data-ttu-id="c4661-112">Der Rückgabewert ist die Länge des Texts in Zeichen, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c4661-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4661-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4661-113">Remarks</span></span>

<span data-ttu-id="c4661-114">Bei einem Bearbeitungs Steuerelement ist der Text, der kopiert werden soll, der Inhalt des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c4661-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="c4661-115">Bei einem Kombinations Feld ist der Text der Inhalt des Bearbeitungs Steuer Elements (oder statischer Text) des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="c4661-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="c4661-116">Für eine Schaltfläche ist der Text der Schaltflächen Name.</span><span class="sxs-lookup"><span data-stu-id="c4661-116">For a button, the text is the button name.</span></span> <span data-ttu-id="c4661-117">Bei anderen Fenstern ist der Text der Fenstertitel.</span><span class="sxs-lookup"><span data-stu-id="c4661-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="c4661-118">Zum Ermitteln der Länge eines Elements in einem Listenfeld kann eine Anwendung die [**\_ gettextlen**](../controls/lb-gettextlen.md) -Nachricht des lb-Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4661-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="c4661-119">Wenn die **WM \_ getTextLength** -Nachricht gesendet wird, gibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Länge des Texts in Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="c4661-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="c4661-120">Unter bestimmten Bedingungen gibt die **defwindowproc** -Funktion einen Wert zurück, der größer ist als die tatsächliche Textlänge.</span><span class="sxs-lookup"><span data-stu-id="c4661-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="c4661-121">Dies tritt bei bestimmten Kombinationen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das System das vorhanden sein von DBCS-Zeichen (Double-Byte Character Set) im Text zulässt.</span><span class="sxs-lookup"><span data-stu-id="c4661-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="c4661-122">Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Textlänge. Sie können Sie daher immer verwenden, um die Puffer Zuordnung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c4661-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="c4661-123">Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialogfelder verwendet, die Unicode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4661-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="c4661-124">Um die genaue Länge des Texts zu erhalten, verwenden Sie die Nachrichten [**WM \_ gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)oder [**CB \_ getlbtext**](../controls/cb-getlbtext.md) oder die Funktion [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="c4661-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="c4661-125">Das Senden einer **WM- \_ getTextLength** -Nachricht an ein statisches, nicht-Text-Steuerelement, z. b. eine statische Bitmap oder ein statisches Symbol, gibt keinen Zeichen folgen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c4661-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="c4661-126">Stattdessen wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4661-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4661-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4661-127">Requirements</span></span>



| <span data-ttu-id="c4661-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4661-128">Requirement</span></span> | <span data-ttu-id="c4661-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c4661-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4661-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4661-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4661-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4661-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c4661-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4661-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4661-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4661-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4661-134">Header</span><span class="sxs-lookup"><span data-stu-id="c4661-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4661-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c4661-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4661-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4661-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4661-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c4661-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4661-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c4661-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c4661-139">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="c4661-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="c4661-140">**Getwindowtextlength**</span><span class="sxs-lookup"><span data-stu-id="c4661-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="c4661-141">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="c4661-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="c4661-142">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c4661-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4661-143">Windows</span><span class="sxs-lookup"><span data-stu-id="c4661-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="c4661-144">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c4661-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c4661-145">**CB \_ getlbtext**</span><span class="sxs-lookup"><span data-stu-id="c4661-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="c4661-146">**LB- \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="c4661-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="c4661-147">**LB- \_ gettextlen**</span><span class="sxs-lookup"><span data-stu-id="c4661-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
