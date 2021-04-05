---
description: Kopiert den Text, der einem Fenster entspricht, in einen Puffer, der vom Aufrufer bereitgestellt wird.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: WM_GETTEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757824"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="5c818-103">WM- \_ gettext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5c818-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="5c818-104">Kopiert den Text, der einem Fenster entspricht, in einen Puffer, der vom Aufrufer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c818-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="5c818-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c818-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c818-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c818-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c818-107">Die maximale Anzahl der zu kopierenden Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5c818-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="5c818-108">Bei ANSI-Anwendungen kann die Größe der Zeichenfolge im Puffer (auf mindestens die Hälfte des Werts des *wParam* -Werts) aufgrund der Konvertierung von ANSI in Unicode reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="5c818-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="5c818-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c818-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c818-110">Ein Zeiger auf den Puffer, der den Text empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="5c818-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c818-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c818-111">Return value</span></span>

<span data-ttu-id="5c818-112">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c818-112">Type: **LRESULT**</span></span>

<span data-ttu-id="5c818-113">Der Rückgabewert ist die Anzahl der kopierten Zeichen, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5c818-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c818-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c818-114">Remarks</span></span>

<span data-ttu-id="5c818-115">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion kopiert den dem Fenster zugeordneten Text in den angegebenen Puffer und gibt die Anzahl der kopierten Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="5c818-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="5c818-116">Beachten Sie, dass für statische nicht-Text-Steuerelemente der Text, mit dem das Steuerelement ursprünglich erstellt wurde, d. h. die ID-Nummer, angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5c818-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="5c818-117">Sie erhalten jedoch die ID des statischen nicht-Text-Steuer Elements, das ursprünglich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c818-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="5c818-118">Das heißt, wenn Sie anschließend ein STM-Abbild verwenden, um es zu ändern, wird die ursprüngliche ID weiterhin zurückgegeben. **\_**</span><span class="sxs-lookup"><span data-stu-id="5c818-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="5c818-119">Bei einem Bearbeitungs Steuerelement ist der Text, der kopiert werden soll, der Inhalt des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="5c818-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="5c818-120">Bei einem Kombinations Feld ist der Text der Inhalt des Bearbeitungs Steuer Elements (oder statischer Text) des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="5c818-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="5c818-121">Für eine Schaltfläche ist der Text der Schaltflächen Name.</span><span class="sxs-lookup"><span data-stu-id="5c818-121">For a button, the text is the button name.</span></span> <span data-ttu-id="5c818-122">Bei anderen Fenstern ist der Text der Fenstertitel.</span><span class="sxs-lookup"><span data-stu-id="5c818-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="5c818-123">Um den Text eines Elements in einem Listenfeld zu kopieren, kann eine Anwendung die [**lb- \_ gettext**](../controls/lb-gettext.md) -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c818-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="5c818-124">Wenn die **WM- \_ gettext** -Nachricht mit dem SS-Symbolstil an ein statisches Steuerelement gesendet wird, wird in den ersten vier Bytes des Puffers, auf die von *LPARAM* verwiesen wird, ein Handle für das Symbol zurückgegeben. **\_**</span><span class="sxs-lookup"><span data-stu-id="5c818-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="5c818-125">Dies gilt nur, wenn die [**WM- \_ SetText**](wm-settext.md) -Nachricht verwendet wurde, um das Symbol festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5c818-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="5c818-126">Umfassende **Bearbeitung:** Wenn der zu kopierende Text 64 KB überschreitet, verwenden Sie entweder die [**EM- \_ StreamOut**](../controls/em-streamout.md) -oder die [**EM \_ GetSelText**](../controls/em-getseltext.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5c818-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="5c818-127">Das Senden einer **WM- \_ gettext** -Nachricht an ein statisches nicht-Text-Steuerelement, z. b. eine statische Bitmap oder ein statisches Symbol Steuerelement, gibt keinen Zeichen folgen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c818-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="5c818-128">Stattdessen wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c818-128">Instead, it returns zero.</span></span> <span data-ttu-id="5c818-129">Außerdem könnten in früheren Versionen von Windows Anwendungen eine **WM- \_ gettext** -Nachricht an ein statisches nicht-Text-Steuerelement senden, um die ID des Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c818-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="5c818-130">Zum Abrufen der ID eines Steuer Elements können Anwendungen [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) mit der **GWL- \_ ID** als Indexwert oder [**getwindowlongptr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) mithilfe der **gwlp- \_ ID** verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c818-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c818-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c818-131">Requirements</span></span>



| <span data-ttu-id="5c818-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c818-132">Requirement</span></span> | <span data-ttu-id="5c818-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5c818-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c818-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c818-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5c818-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c818-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5c818-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c818-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5c818-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c818-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5c818-138">Header</span><span class="sxs-lookup"><span data-stu-id="5c818-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c818-139"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5c818-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c818-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c818-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c818-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5c818-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c818-142">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5c818-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5c818-143">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="5c818-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="5c818-144">**Getwindowlongptr**</span><span class="sxs-lookup"><span data-stu-id="5c818-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="5c818-145">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="5c818-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="5c818-146">**Getwindowtextlength**</span><span class="sxs-lookup"><span data-stu-id="5c818-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="5c818-147">**WM \_ getTextLength**</span><span class="sxs-lookup"><span data-stu-id="5c818-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="5c818-148">**WM- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="5c818-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="5c818-149">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5c818-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c818-150">Windows</span><span class="sxs-lookup"><span data-stu-id="5c818-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="5c818-151">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5c818-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5c818-152">**EM \_ GetSelText**</span><span class="sxs-lookup"><span data-stu-id="5c818-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="5c818-153">**EM- \_ StreamOut**</span><span class="sxs-lookup"><span data-stu-id="5c818-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="5c818-154">**LB- \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="5c818-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 
