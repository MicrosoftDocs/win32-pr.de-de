---
title: EM_AUTOURLDETECT Meldung (RichEdit. h)
description: Aktiviert oder deaktiviert die automatische Erkennung von Hyperlinks von einem Rich-Edit-Steuerelement.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Windows-Steuerelemente für EM_AUTOURLDETECT Meldung
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956730"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="68577-104">EM \_ autourldetect-Meldung</span><span class="sxs-lookup"><span data-stu-id="68577-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="68577-105">Aktiviert oder deaktiviert die automatische Erkennung von Hyperlinks von einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="68577-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="68577-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68577-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68577-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68577-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68577-108">Geben Sie 0 an, um die automatische Link Erkennung zu deaktivieren, oder einen der folgenden Werte, um verschiedene Arten von Erkennung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="68577-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="68577-109">Wert</span><span class="sxs-lookup"><span data-stu-id="68577-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="68577-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="68577-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="68577-111"><dt>**aurl \_ disablemixedlgc**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="68577-112">**Windows 8**: Deaktivieren Sie die Erkennung von Domänen Namen, die Bezeichnungen mit Zeichen enthalten, die zu mehr als einem der folgenden Skripts gehören: Lateinisch, Griechisch und Kyrillisch.</span><span class="sxs-lookup"><span data-stu-id="68577-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="68577-113"><dt>**aurl- \_ enabledriveletters**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="68577-114">**Windows 8**: Erkennen von Dateinamen mit einer führenden Laufwerk Spezifikation, z. b. "c: \\ Temp".</span><span class="sxs-lookup"><span data-stu-id="68577-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="68577-115"><dt>**aurl- \_ enableea**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="68577-116">Dieser Wert ist veraltet. Verwenden Sie stattdessen **aurl- \_ enableeaurls** .</span><span class="sxs-lookup"><span data-stu-id="68577-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="68577-117"><dt>**aurl- \_ enableeaurls**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="68577-118">Erkennen von URLs, die ostasiatische Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="68577-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="68577-119"><dt>**aurl \_ enableemailaddr**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="68577-120">**Windows 8**: Erkennen von e-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="68577-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="68577-121"><dt>**aurl- \_ enabletelno**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="68577-122">**Windows 8**: Erkennen von Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="68577-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="68577-123"><dt>**aurl- \_ EnableURL**</dt></span><span class="sxs-lookup"><span data-stu-id="68577-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="68577-124">**Windows 8**: erkennen Sie URLs, die den Pfad enthalten.</span><span class="sxs-lookup"><span data-stu-id="68577-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="68577-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68577-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68577-126">Dieser Parameter bestimmt die URL-Schemas, die erkannt werden, wenn **aurl- \_ EnableURL** aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="68577-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="68577-127">Wenn *LPARAM* den Wert NULL hat, wird die Liste der Standardschema Namen verwendet (siehe Hinweise).</span><span class="sxs-lookup"><span data-stu-id="68577-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="68577-128">Alternativ kann *LPARAM* auf eine mit NULL endenden Zeichenfolge zeigen, die aus bis zu 50 durch Doppelpunkten beendeten Schema Namen besteht, die die Standardschema Namen Liste ablösen.</span><span class="sxs-lookup"><span data-stu-id="68577-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="68577-129">Die Zeichenfolge könnte z. b. "News: http: FTP: Telnet:" lauten.</span><span class="sxs-lookup"><span data-stu-id="68577-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="68577-130">Die Schema Namen Syntax ist in der Website der Internet Engineering Task Force (IETF)-Website in der [URI (Uniform Resource Identifier): Generisches Syntax]( https://www.ietf.org/rfc/rfc2396.txt) Dokument definiert.</span><span class="sxs-lookup"><span data-stu-id="68577-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="68577-131">Ein Schema Name kann beispielsweise bis zu 13 Zeichen (einschließlich des Doppelpunkts) enthalten, muss mit einem alphabetischen ASCII-Wert beginnen. Anschließend kann eine Mischung aus ASCII-alphabetik, Ziffern und den drei Interpunktions Zeichen folgen: ".", "+" und "-".</span><span class="sxs-lookup"><span data-stu-id="68577-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="68577-132">Der Zeichen folgertyp kann entweder \*\* \* char\* _ oder _*WCHAR \**_ lauten; das Rich Edit-Steuerelement erkennt den Typ automatisch.</span><span class="sxs-lookup"><span data-stu-id="68577-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68577-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68577-133">Return value</span></span>

<span data-ttu-id="68577-134">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="68577-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="68577-135">Wenn die Meldung fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="68577-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="68577-136">Beispielsweise kann die Nachricht aufgrund von unzureichendem Arbeitsspeicher, einer ungültigen Erkennungs Option oder einer ungültigen Schema namens Zeichenfolge fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="68577-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="68577-137">Wenn _lParam \* mehr als 50 Schema Namen enthält, schlägt die Nachricht mit dem Rückgabewert **E \_ invalidArg** fehl.</span><span class="sxs-lookup"><span data-stu-id="68577-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68577-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68577-138">Remarks</span></span>

<span data-ttu-id="68577-139">Wenn die automatische URL-Erkennung aktiviert ist (d. h., *wParam* enthält **aurl- \_ EnableURL**), scannt das Rich Edit-Steuerelement den geänderten Text, um zu bestimmen, ob der Text mit dem Format einer URL übereinstimmt (oder allgemeiner in Windows 8 oder höher eine IRI International Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="68577-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="68577-140">Wenn *LPARAM* den Wert NULL hat, erkennt das-Steuerelement URLs, die mit den folgenden Schema Namen beginnen:</span><span class="sxs-lookup"><span data-stu-id="68577-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="68577-141">callto</span><span class="sxs-lookup"><span data-stu-id="68577-141">callto</span></span>
-   <span data-ttu-id="68577-142">file</span><span class="sxs-lookup"><span data-stu-id="68577-142">file</span></span>
-   <span data-ttu-id="68577-143">ftp</span><span class="sxs-lookup"><span data-stu-id="68577-143">ftp</span></span>
-   <span data-ttu-id="68577-144">Gopher</span><span class="sxs-lookup"><span data-stu-id="68577-144">gopher</span></span>
-   <span data-ttu-id="68577-145">http</span><span class="sxs-lookup"><span data-stu-id="68577-145">http</span></span>
-   <span data-ttu-id="68577-146">https</span><span class="sxs-lookup"><span data-stu-id="68577-146">https</span></span>
-   <span data-ttu-id="68577-147">mailto</span><span class="sxs-lookup"><span data-stu-id="68577-147">mailto</span></span>
-   <span data-ttu-id="68577-148">news</span><span class="sxs-lookup"><span data-stu-id="68577-148">news</span></span>
-   <span data-ttu-id="68577-149">notes</span><span class="sxs-lookup"><span data-stu-id="68577-149">notes</span></span>
-   <span data-ttu-id="68577-150">NNTP-</span><span class="sxs-lookup"><span data-stu-id="68577-150">nntp</span></span>
-   <span data-ttu-id="68577-151">onenote</span><span class="sxs-lookup"><span data-stu-id="68577-151">onenote</span></span>
-   <span data-ttu-id="68577-152">positiv</span><span class="sxs-lookup"><span data-stu-id="68577-152">outlook</span></span>
-   <span data-ttu-id="68577-153">Prospero</span><span class="sxs-lookup"><span data-stu-id="68577-153">prospero</span></span>
-   <span data-ttu-id="68577-154">tel</span><span class="sxs-lookup"><span data-stu-id="68577-154">tel</span></span>
-   <span data-ttu-id="68577-155">telnet</span><span class="sxs-lookup"><span data-stu-id="68577-155">telnet</span></span>
-   <span data-ttu-id="68577-156">wais</span><span class="sxs-lookup"><span data-stu-id="68577-156">wais</span></span>
-   <span data-ttu-id="68577-157">webcal</span><span class="sxs-lookup"><span data-stu-id="68577-157">webcal</span></span>

<span data-ttu-id="68577-158">Wenn die automatische Verknüpfungs Erkennung aktiviert ist, entfernt das Rich Edit-Steuerelement den **CFE- \_ Link** Effekt aus dem geänderten Text, der nicht vom Steuerelement erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="68577-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="68577-159">Aktivieren Sie die automatische Link Erkennung nicht, wenn Ihre Anwendung den **CFE- \_ Link** Effekt verwendet, um andere Text Typen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="68577-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="68577-160">Das Rich Edit-Steuerelement prüft nicht, ob ein erkannter Link vorhanden ist. Diese Verantwortung gehört zum Client.</span><span class="sxs-lookup"><span data-stu-id="68577-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="68577-161">Wenn ein Rich-Edit-Steuerelement den Mauszeiger über Text mit dem **Link "CFE- \_ Link** " empfängt, sendet er eine Benachrichtigung über den [ \_ Link "en](en-link.md) ".</span><span class="sxs-lookup"><span data-stu-id="68577-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="68577-162">Weitere Informationen finden Sie unter [Automatische RichEdit-Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) und [RichEdit-Anzeige Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span><span class="sxs-lookup"><span data-stu-id="68577-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="68577-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68577-163">Requirements</span></span>



| <span data-ttu-id="68577-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68577-164">Requirement</span></span> | <span data-ttu-id="68577-165">Wert</span><span class="sxs-lookup"><span data-stu-id="68577-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68577-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68577-166">Minimum supported client</span></span><br/> | <span data-ttu-id="68577-167">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68577-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68577-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68577-168">Minimum supported server</span></span><br/> | <span data-ttu-id="68577-169">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68577-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68577-170">Header</span><span class="sxs-lookup"><span data-stu-id="68577-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="68577-171"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="68577-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68577-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68577-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68577-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="68577-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="68577-174">Link "en" \_</span><span class="sxs-lookup"><span data-stu-id="68577-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

