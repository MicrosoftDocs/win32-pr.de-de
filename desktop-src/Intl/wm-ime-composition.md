---
description: Wird an eine Anwendung gesendet, wenn der IME den Kompositions Status als Ergebnis einer Tastatureingabe ändert. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: WM_IME_COMPOSITION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960924"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="fd5be-104">WM \_ IME- \_ Kompositions Nachricht</span><span class="sxs-lookup"><span data-stu-id="fd5be-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="fd5be-105">Wird an eine Anwendung gesendet, wenn der IME den Kompositions Status als Ergebnis einer Tastatureingabe ändert.</span><span class="sxs-lookup"><span data-stu-id="fd5be-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="fd5be-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fd5be-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="fd5be-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd5be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd5be-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fd5be-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fd5be-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="fd5be-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="fd5be-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd5be-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd5be-111">DBCS-Zeichen, das die letzte Änderung an der Kompositions Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="fd5be-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="fd5be-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd5be-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd5be-113">Ein Wert, der angibt, wie die Kompositions Zeichenfolge oder das Zeichen</span><span class="sxs-lookup"><span data-stu-id="fd5be-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="fd5be-114">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fd5be-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="fd5be-115">Weitere Informationen zu diesen Werten finden Sie unter [IME-Kompositions Zeichen folgen Werte](ime-composition-string-values.md).</span><span class="sxs-lookup"><span data-stu-id="fd5be-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="fd5be-116">**GCS- \_ compattr**</span><span class="sxs-lookup"><span data-stu-id="fd5be-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="fd5be-117">**GCS- \_ compclause**</span><span class="sxs-lookup"><span data-stu-id="fd5be-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="fd5be-118">**GCS- \_ compreadstr**</span><span class="sxs-lookup"><span data-stu-id="fd5be-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="fd5be-119">**GCS- \_ compreadattr**</span><span class="sxs-lookup"><span data-stu-id="fd5be-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="fd5be-120">**GCS- \_ compreadclause**</span><span class="sxs-lookup"><span data-stu-id="fd5be-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="fd5be-121">**GCS \_ compstr**</span><span class="sxs-lookup"><span data-stu-id="fd5be-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="fd5be-122">**GCS- \_ Cursor**</span><span class="sxs-lookup"><span data-stu-id="fd5be-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="fd5be-123">**GCS \_ Delta Start**</span><span class="sxs-lookup"><span data-stu-id="fd5be-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="fd5be-124">**GCS- \_ resultclause**</span><span class="sxs-lookup"><span data-stu-id="fd5be-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="fd5be-125">**GCS- \_ resultreadclause**</span><span class="sxs-lookup"><span data-stu-id="fd5be-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="fd5be-126">**GCS- \_ resultreadstr**</span><span class="sxs-lookup"><span data-stu-id="fd5be-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="fd5be-127">**GCS- \_ ResultStr**</span><span class="sxs-lookup"><span data-stu-id="fd5be-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="fd5be-128">Der *LPARAM* -Parameter kann auch einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fd5be-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="fd5be-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fd5be-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="fd5be-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fd5be-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="fd5be-131"><dt>**CS- \_ insertchar**</dt></span><span class="sxs-lookup"><span data-stu-id="fd5be-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="fd5be-132">Fügen Sie das *wParam* -Kompositions Zeichen an der aktuellen Einfügemarke ein.</span><span class="sxs-lookup"><span data-stu-id="fd5be-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="fd5be-133">Eine Anwendung sollte das Kompositions Zeichen anzeigen, wenn diese Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd5be-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="fd5be-134"><dt>**CS \_ nomovecaret**</dt></span><span class="sxs-lookup"><span data-stu-id="fd5be-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="fd5be-135">Verschieben Sie die Position der Einfügemarke nicht als Ergebnis der Verarbeitung der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fd5be-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="fd5be-136">Wenn ein IME z. b. eine Kombination aus CS \_ insertchar und CS \_ nomovecaret angibt, sollte die Anwendung das angegebene Zeichen an der aktuellen Position der Einfügemarke einfügen, aber die Einfügemarke nicht an die nächste Position verschieben.</span><span class="sxs-lookup"><span data-stu-id="fd5be-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="fd5be-137">Diese Zeichenfolge wird durch eine nachfolgende WM \_ IME- \_ Kompositions Nachricht mit GCS \_ ResultStr ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fd5be-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd5be-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd5be-138">Return value</span></span>

<span data-ttu-id="fd5be-139">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="fd5be-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd5be-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd5be-140">Remarks</span></span>

<span data-ttu-id="fd5be-141">Eine Anwendung sollte diese Nachricht verarbeiten, wenn Sie selbst Kompositions Zeichen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fd5be-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="fd5be-142">Andernfalls sollte die Nachricht an das IME-Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd5be-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="fd5be-143">Wenn die Anwendung ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fd5be-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="fd5be-144">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion verarbeitet diese Nachricht, indem Sie Sie an das IME-Standardfenster übergibt.</span><span class="sxs-lookup"><span data-stu-id="fd5be-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="fd5be-145">Das IME-Fenster verarbeitet diese Nachricht, indem seine Darstellung basierend auf dem angegebenen Änderungsflag aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="fd5be-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="fd5be-146">Eine Anwendung kann " [**immgetcompositionstring**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) " aufrufen, um den neuen Kompositions Status abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd5be-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="fd5be-147">Wenn keiner der GCS \_ -Werte festgelegt wird, gibt die Meldung an, dass die aktuelle Komposition abgebrochen wurde, und Anwendungen, die die Kompositions Zeichenfolge zeichnen, sollten die Zeichenfolge löschen.</span><span class="sxs-lookup"><span data-stu-id="fd5be-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5be-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd5be-148">Requirements</span></span>



| <span data-ttu-id="fd5be-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd5be-149">Requirement</span></span> | <span data-ttu-id="fd5be-150">Wert</span><span class="sxs-lookup"><span data-stu-id="fd5be-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5be-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd5be-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5be-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd5be-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="fd5be-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd5be-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5be-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd5be-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="fd5be-155">Header</span><span class="sxs-lookup"><span data-stu-id="fd5be-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd5be-156"><dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd5be-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd5be-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd5be-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5be-158">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="fd5be-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="fd5be-159">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="fd5be-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="fd5be-160">**ImmGetCompositionString**</span><span class="sxs-lookup"><span data-stu-id="fd5be-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
