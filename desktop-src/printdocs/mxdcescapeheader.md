---
description: Die mxdc- \_ Escape-Header-T- \_ \_ Struktur enthält den Vorgangs Code für einen extescape-extescape mit mxdc-Escapezeichen \_ als Nescape-Parameter. Außerdem werden die Größen der Eingabe-und Ausgabepuffer bereitstellt.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868528"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="62586-104">Mxdc- \_ Escape-Header-T- \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="62586-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="62586-105">Die **mxdc- \_ Escape- \_ Header- \_ T** -Struktur enthält den Vorgangs Code für einen [**extescape-extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit [**mxdc \_**](mxdc-escape.md) -Escapezeichen als *Nescape* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="62586-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="62586-106">Außerdem werden die Größen der Eingabe-und Ausgabepuffer bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="62586-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="62586-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62586-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="62586-108">Member</span><span class="sxs-lookup"><span data-stu-id="62586-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="62586-109">**cbinput**</span><span class="sxs-lookup"><span data-stu-id="62586-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="62586-110">Die Größe des Eingabe Puffers, der an den *lpszoutdata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="62586-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="62586-111">**cboutput**</span><span class="sxs-lookup"><span data-stu-id="62586-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="62586-112">Die Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="62586-112">The size of the output buffer.</span></span> <span data-ttu-id="62586-113">Dies ist der gleiche Wert wie der *cboutput* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="62586-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="62586-114">**opCode**</span><span class="sxs-lookup"><span data-stu-id="62586-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="62586-115">Die Code Konstante, die mxdc mitteilt, was zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="62586-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="62586-116">Vorgangs Code</span><span class="sxs-lookup"><span data-stu-id="62586-116">Operations code</span></span>                      | <span data-ttu-id="62586-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62586-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62586-118">mxdcop \_ get \_ filename</span><span class="sxs-lookup"><span data-stu-id="62586-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="62586-119">Gibt im *lpszoutdata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion entweder den vollständigen Pfad der Ausgabedatei als NULL-terminierte Zeichenfolge oder die Größe der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="62586-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="62586-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="62586-120">See Remarks.</span></span>                   |
| <span data-ttu-id="62586-121">mxdcop \_ PrintTicket \_ festes \_ doc-Dokument \_</span><span class="sxs-lookup"><span data-stu-id="62586-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="62586-122">Ordnet ein Druck Ticket einer XPS-Fixed-Dokument Sequenz zu.</span><span class="sxs-lookup"><span data-stu-id="62586-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="62586-123">Festes doc für mxdcop \_ PrintTicket \_ \_</span><span class="sxs-lookup"><span data-stu-id="62586-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="62586-124">Verknüpft ein Druck Ticket mit einem XPS-Dokument.</span><span class="sxs-lookup"><span data-stu-id="62586-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="62586-125">Fixed-Seite für mxdcop \_ PrintTicket \_ \_</span><span class="sxs-lookup"><span data-stu-id="62586-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="62586-126">Ordnet ein Druck Ticket einer XPS-Seite zu.</span><span class="sxs-lookup"><span data-stu-id="62586-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="62586-127">Mxdcop \_ Set \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="62586-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="62586-128">Sendet das XPS-Markup der aktuellen Seite an die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="62586-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="62586-129">Mxdcop \_ Set \_ S0PAGE- \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="62586-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="62586-130">Sendet eine Ressource auf der Seite, z. b. ein Bild oder eine Schriftart, an die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="62586-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="62586-131">mxdcop- \_ Set- \_ xpspassthru- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="62586-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="62586-132">Versetzt den mxdc in einen Pass-Through-Zustand, sodass eine Anwendung XPS direkt in die Ausgabedatei schreiben kann, ohne dass der mxdc verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="62586-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="62586-133">Auf diese Weise kann ein gesamtes Dokument oder sogar eine Dokument Sequenz geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="62586-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62586-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62586-134">Remarks</span></span>

<span data-ttu-id="62586-135">Vor dem Aufrufen von [**mxdc \_**](mxdc-escape.md)-Escapezeichen \_ sollten Anwendungen zuerst überprüfen, ob der Treiber mxdc ist, indem Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) -Escapezeichen aufrufen</span><span class="sxs-lookup"><span data-stu-id="62586-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="62586-136">Wenn der Treiber der mxdc ist, gibt die Funktion die mit 0 (null) beendete Zeichenfolge " http://schemas.microsoft.com/xps/2005/06 " zurück.</span><span class="sxs-lookup"><span data-stu-id="62586-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="62586-137">Diese Struktur befindet sich immer am Anfang der Daten, die in Ihrem *lpszindata* -Parameter an die [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="62586-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="62586-138">Wenn **Opcode** "mxdcop \_ get \_ filename" ist:</span><span class="sxs-lookup"><span data-stu-id="62586-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="62586-139">Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht nur aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="62586-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="62586-140">Rufen Sie den Ausgabedatei Namen ab, indem Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zweimal aufrufen.</span><span class="sxs-lookup"><span data-stu-id="62586-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="62586-141">Übergeben Sie beim ersten Mal 4 an den *cboutput* -Parameter von [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="62586-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="62586-142">Legen Sie den *lpszoutdata* -Parameter so fest, dass er auf zugeordnete 4 Bytes an Arbeitsspeicher verweist.</span><span class="sxs-lookup"><span data-stu-id="62586-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="62586-143">Der voll qualifizierte Dateipfad wird im *lpszoutdata* -Parameter von **extescape** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62586-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="62586-144">Anschließend wird die Funktion erneut aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="62586-144">Then call the function again.</span></span> <span data-ttu-id="62586-145">Legen Sie diesmal sowohl *cboutput* als auch *cbinput* auf 4 + *DataSize* fest.</span><span class="sxs-lookup"><span data-stu-id="62586-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="62586-146">Der voll qualifizierte Dateipfad wird in einer [**mxdcgetfileamedata**](mxdcgetfilenamedata.md) -Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62586-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="62586-147">Wenn **Opcode** "mxdcop \_ PrintTicket \_ Fixed \_ doc/ \_ q" oder "mxdcop \_ PrintTicket \_ Fixed \_ doc" ist:</span><span class="sxs-lookup"><span data-stu-id="62586-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="62586-148">Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**mxdcprintticketpassthrough**](mxdcprintticketpassthrough.md) -Struktur, die in eine [**mxdcprintticketescape**](mxdcprintticketescape.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="62586-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="62586-149">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) und einem- [**Endpunkt**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)auftreten.</span><span class="sxs-lookup"><span data-stu-id="62586-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="62586-150">Wenn **Opcode** die festgelegte mxdcop- \_ PrintTicket- \_ Seite ist \_ :</span><span class="sxs-lookup"><span data-stu-id="62586-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="62586-151">Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**mxdcprintticketpassthrough**](mxdcprintticketpassthrough.md) -Struktur, die in eine [**mxdcprintticketescape**](mxdcprintticketescape.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="62586-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="62586-152">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="62586-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="62586-153">Wenn **Opcode** auf mxdcop \_ festgelegt ist \_ S0PAGE:</span><span class="sxs-lookup"><span data-stu-id="62586-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="62586-154">Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**MxdcS0PageData**](mxdcs0pagedata.md) -Struktur, die in eine [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="62586-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="62586-155">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="62586-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="62586-156">Die aufrufende Anwendung ist für die Validierung des XML-Codes verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="62586-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="62586-157">Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit mxdcop \_ Set \_ S0PAGE \_ Resource als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit mxdcop \_ Set S0PAGE aufzurufen \_ .</span><span class="sxs-lookup"><span data-stu-id="62586-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="62586-158">Wenn **Opcode** auf mxdcop \_ Set \_ S0PAGE Resource festgelegt ist \_ :</span><span class="sxs-lookup"><span data-stu-id="62586-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="62586-159">Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) -Struktur, die in eine [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) -Struktur verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="62586-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="62586-160">Der Aufruf von [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen, aber es können mehrere solcher Aufrufe zwischen den Aufrufen **Startpage** und **EndPage** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="62586-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="62586-161">Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit mxdcop \_ Set \_ S0PAGE \_ Resource als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit mxdcop \_ Set S0PAGE aufzurufen \_ .</span><span class="sxs-lookup"><span data-stu-id="62586-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="62586-162">Wenn **Opcode** auf mxdcop festgelegt ist, wird der \_ \_ xpspassthru- \_ Modus ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="62586-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="62586-163">Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht nur aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="62586-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="62586-164">Dieser Rückruf muss vor dem Aufrufen von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="62586-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="62586-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62586-165">Requirements</span></span>



| <span data-ttu-id="62586-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62586-166">Requirement</span></span> | <span data-ttu-id="62586-167">Wert</span><span class="sxs-lookup"><span data-stu-id="62586-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="62586-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62586-168">Minimum supported client</span></span><br/> | <span data-ttu-id="62586-169">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62586-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62586-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62586-170">Minimum supported server</span></span><br/> | <span data-ttu-id="62586-171">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62586-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62586-172">Header</span><span class="sxs-lookup"><span data-stu-id="62586-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="62586-173"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="62586-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62586-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62586-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62586-175">Drucken</span><span class="sxs-lookup"><span data-stu-id="62586-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="62586-176">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="62586-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="62586-177">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62586-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="62586-178">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="62586-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="62586-179">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="62586-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

