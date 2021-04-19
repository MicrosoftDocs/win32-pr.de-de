---
description: Mithilfe der escapefunktion "mxdc \_ Escape Printer" können Anwendungen Dokumente in eine Datei oder einen Drucker im XPS-Format (XML Paper Specification) über den Microsoft XPS Document Converter (mxdc) schreiben.
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE-Funktion (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363458"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="dd297-103">Mxdc- \_ Escape-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd297-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="dd297-104">Mithilfe der escapefunktion " **mxdc \_ Escape** Printer" können Anwendungen Dokumente in eine Datei oder einen Drucker im XPS-Format (XML Paper Specification) über den Microsoft XPS Document Converter (mxdc) schreiben.</span><span class="sxs-lookup"><span data-stu-id="dd297-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="dd297-105">Um diesen Vorgang auszuführen, nennen Sie die [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion mit den folgenden Parametern.</span><span class="sxs-lookup"><span data-stu-id="dd297-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd297-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd297-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="dd297-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd297-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd297-108">*HDC*</span><span class="sxs-lookup"><span data-stu-id="dd297-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="dd297-109">Ein Handle für den Drucker Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="dd297-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="dd297-110">*cbinput*</span><span class="sxs-lookup"><span data-stu-id="dd297-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="dd297-111">Die Größe (in Bytes) der Daten, auf die durch den *lpszindata* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dd297-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dd297-112">*lpszindata*</span><span class="sxs-lookup"><span data-stu-id="dd297-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="dd297-113">Ein Zeiger auf einen Puffer, der die Eingabedaten enthält, die immer in einer der folgenden-Strukturen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dd297-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="dd297-114"><a href="mxdcescapeheader.md">**Mxdcescapeheader**</a></span><span class="sxs-lookup"><span data-stu-id="dd297-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="dd297-115"><a href="mxdcprintticketescape.md">**Mxdcprintticketescape**</a></span><span class="sxs-lookup"><span data-stu-id="dd297-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="dd297-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="dd297-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="dd297-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="dd297-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="dd297-118">Jede dieser Strukturen verfügt über einen OpCode-Member, der angibt, was der mxdc tun soll.</span><span class="sxs-lookup"><span data-stu-id="dd297-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="dd297-119">Ausführliche Hinweise zu diesen Codes finden Sie unter mxdcescapeheader.</span><span class="sxs-lookup"><span data-stu-id="dd297-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="dd297-120">Vorgangs Code (OpCode)</span><span class="sxs-lookup"><span data-stu-id="dd297-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="dd297-121">Aktion</span><span class="sxs-lookup"><span data-stu-id="dd297-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="dd297-122"><dt>**mxdcop \_ get \_ filename**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="dd297-123">Legt den *lpszoutdata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion auf fest, entweder den vollständigen Pfad der Ausgabedatei als NULL-terminierte Zeichenfolge oder andernfalls die Größe dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dd297-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="dd297-124"><dt>**mxdcop \_ PrintTicket \_ festes \_ doc-Dokument \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="dd297-125">Ordnet ein Druck Ticket einer XPS-Fixed-Dokument Sequenz zu.</span><span class="sxs-lookup"><span data-stu-id="dd297-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="dd297-126"><dt>**Festes doc für mxdcop \_ PrintTicket \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="dd297-127">Verknüpft ein Druck Ticket mit einem XPS-Dokument.</span><span class="sxs-lookup"><span data-stu-id="dd297-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="dd297-128"><dt>**Fixed-Seite für mxdcop \_ PrintTicket \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="dd297-129">Ordnet ein Druck Ticket einer XPS-Seite zu.</span><span class="sxs-lookup"><span data-stu-id="dd297-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="dd297-130"><dt>**Mxdcop \_ Set \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="dd297-131">Sendet das XPS-Markup der aktuellen Seite an die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="dd297-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="dd297-132"><dt>**Mxdcop \_ Set \_ S0PAGE- \_ Ressource**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="dd297-133">Sendet eine Ressource auf der Seite, z. b. ein Bild oder eine Schriftart, an die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="dd297-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="dd297-134"><dt>**mxdcop- \_ Set- \_ xpspassthru- \_ Modus**</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="dd297-135">Versetzt den mxdc in einen Pass-Through-Zustand, sodass eine Anwendung XPS direkt in die Ausgabedatei schreiben kann, ohne dass der mxdc verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="dd297-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="dd297-136">Auf diese Weise kann ein gesamtes Dokument oder sogar eine Dokument Sequenz geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd297-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dd297-137">*cboutput*</span><span class="sxs-lookup"><span data-stu-id="dd297-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="dd297-138">Die Größe (in Bytes) der Daten, auf die durch den *lpszoutdata* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dd297-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dd297-139">*lpszoutdata*</span><span class="sxs-lookup"><span data-stu-id="dd297-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="dd297-140">Ein Zeiger auf einen Puffer, der die Ausgabedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="dd297-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd297-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd297-141">Return value</span></span>

<span data-ttu-id="dd297-142">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dd297-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="dd297-143">Wenn die Funktion fehlschlägt oder nicht unterstützt wird, ist der Rückgabewert kleiner oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dd297-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd297-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd297-144">Remarks</span></span>

<span data-ttu-id="dd297-145">Diese Escapesequenz wird von mxdc und XPSDrv unterstützt, aber nicht durch GDI.</span><span class="sxs-lookup"><span data-stu-id="dd297-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="dd297-146">Um zu ermitteln, ob der Druckertreiber der mxdc ist, nennen Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit der [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) -Escapezeichen.</span><span class="sxs-lookup"><span data-stu-id="dd297-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="dd297-147">Wenn der Treiber der mxdc ist, gibt " **extescape** " die mit 0 (null) beendete Zeichenfolge ("") zurück http://schemas.microsoft.com/xps/2005/06 .</span><span class="sxs-lookup"><span data-stu-id="dd297-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="dd297-148">Stellen Sie sicher, dass der vom *lpszoutdata* -Parameter referenzierte Puffer groß genug ist, um diese Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dd297-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="dd297-149">Vergewissern Sie sich, dass es sich bei dem Druckertreiber um den Microsoft XPS Document Writer-Treiber handelt, um zu bestimmen, ob es sich bei dem Druckertreiber um den mxdc handelt, und legen Sie dann fest, ob der Name des Druckertreibers "Microsoft XPS Document Writer" ist.</span><span class="sxs-lookup"><span data-stu-id="dd297-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="dd297-150">Verwenden Sie eine der folgenden Verfahren, um den Namen des Druckertreibers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dd297-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="dd297-151">Aufrufen von [**getprinterdriver**](getprinterdriver.md) , bei dem der *Level* -Parameter auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dd297-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="dd297-152">Der Name des Druckertreibers wird im Mitglied " **PName** " der Struktur " [**Driver \_ Info \_ 1**](driver-info-1.md) " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd297-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="dd297-153">oder</span><span class="sxs-lookup"><span data-stu-id="dd297-153">or</span></span>  
<span data-ttu-id="dd297-154">Ruft [**GetPrinter**](getprinter.md) auf, wobei der *Level* -Parameter auf 2 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dd297-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="dd297-155">Der Name des Druckertreibers wird im **pdrivername** -Element der [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd297-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="dd297-156">In der folgenden Tabelle wird gezeigt, wo verschiedene Objekte in der XPS-Datei gefunden werden, in der verschiedene Objekttypen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd297-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="dd297-157">Object</span><span class="sxs-lookup"><span data-stu-id="dd297-157">Object</span></span>       | <span data-ttu-id="dd297-158">Speicherort in der Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="dd297-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="dd297-159">Seite "korrigiert"</span><span class="sxs-lookup"><span data-stu-id="dd297-159">Fixed Page</span></span>   | <span data-ttu-id="dd297-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="dd297-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="dd297-161">Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="dd297-161">Thumbnail</span></span>    | <span data-ttu-id="dd297-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="dd297-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="dd297-163">Ticket drucken</span><span class="sxs-lookup"><span data-stu-id="dd297-163">Print Ticket</span></span> | <span data-ttu-id="dd297-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="dd297-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="dd297-165">Schriftart</span><span class="sxs-lookup"><span data-stu-id="dd297-165">Font</span></span>         | <span data-ttu-id="dd297-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="dd297-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="dd297-167">Image</span><span class="sxs-lookup"><span data-stu-id="dd297-167">Image</span></span>        | <span data-ttu-id="dd297-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="dd297-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="dd297-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd297-169">Requirements</span></span>



| <span data-ttu-id="dd297-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd297-170">Requirement</span></span> | <span data-ttu-id="dd297-171">Wert</span><span class="sxs-lookup"><span data-stu-id="dd297-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dd297-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd297-172">Minimum supported client</span></span><br/> | <span data-ttu-id="dd297-173">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd297-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd297-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd297-174">Minimum supported server</span></span><br/> | <span data-ttu-id="dd297-175">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd297-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dd297-176">Header</span><span class="sxs-lookup"><span data-stu-id="dd297-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd297-177"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd297-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd297-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd297-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd297-179">Drucken</span><span class="sxs-lookup"><span data-stu-id="dd297-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="dd297-180">[Druckerescapefunktionen](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd297-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dd297-181">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="dd297-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

