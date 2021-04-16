---
description: Die Drucker \_ Info \_ 2-Struktur gibt ausführliche Drucker Informationen an.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: PRINTER_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529756"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="4c81a-103">Drucker \_ Info \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="4c81a-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="4c81a-104">Die **Drucker \_ Info \_ 2** -Struktur gibt ausführliche Drucker Informationen an.</span><span class="sxs-lookup"><span data-stu-id="4c81a-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c81a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c81a-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="4c81a-106">Member</span><span class="sxs-lookup"><span data-stu-id="4c81a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c81a-107">**pservername**</span><span class="sxs-lookup"><span data-stu-id="4c81a-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Server identifiziert, der den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="4c81a-109">Wenn diese Zeichenfolge **null** ist, wird der Drucker lokal gesteuert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-110">**pprintername**</span><span class="sxs-lookup"><span data-stu-id="4c81a-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-112">**psharename**</span><span class="sxs-lookup"><span data-stu-id="4c81a-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Freigabe Punkt für den Drucker angibt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="4c81a-114">(Diese Zeichenfolge wird nur verwendet, wenn der Drucker \_ \_Die freigegebene Attribut Konstante wurde für den **Attributmember** festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="4c81a-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-115">**pportname**</span><span class="sxs-lookup"><span data-stu-id="4c81a-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-116">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="4c81a-117">Wenn ein Drucker mit mehr als einem Port verbunden ist, müssen die Namen der einzelnen Ports durch Kommas getrennt werden (z. b. "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="4c81a-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-118">**pdrivername**</span><span class="sxs-lookup"><span data-stu-id="4c81a-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckertreibers angibt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-120">**pcomment**</span><span class="sxs-lookup"><span data-stu-id="4c81a-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-121">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die eine kurze Beschreibung des Druckers bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-122">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="4c81a-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-123">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den physischen Speicherort des Druckers angibt (z. b. "Bldg".</span><span class="sxs-lookup"><span data-stu-id="4c81a-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="4c81a-124">38, Raum 1164 ").</span><span class="sxs-lookup"><span data-stu-id="4c81a-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-125">**pdevmode**</span><span class="sxs-lookup"><span data-stu-id="4c81a-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-126">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die Standarddrucker Daten definiert, wie z. b. die Papier Ausrichtung und die Auflösung.</span><span class="sxs-lookup"><span data-stu-id="4c81a-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-127">**psepfile**</span><span class="sxs-lookup"><span data-stu-id="4c81a-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-128">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der Datei angibt, die zum Erstellen der Trenn Zeichenseite verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4c81a-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="4c81a-129">Diese Seite wird verwendet, um Druckaufträge, die an den Drucker gesendet werden, zu trennen.</span><span class="sxs-lookup"><span data-stu-id="4c81a-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-130">**pprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="4c81a-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-131">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des vom Drucker verwendeten Druck Prozessors angibt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="4c81a-132">Mit der [**enumprintprocessor**](enumprintprocessors.md) -Funktion können Sie eine Liste der auf einem Server installierten Druck Prozessoren abrufen.</span><span class="sxs-lookup"><span data-stu-id="4c81a-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-133">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="4c81a-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-134">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c81a-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="4c81a-135">Sie können die [**enumprintprocessordatatypes**](enumprintprocessordatatypes.md) -Funktion verwenden, um eine Liste von Datentypen abzurufen, die von einem bestimmten Druck Prozessor unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-136">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="4c81a-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-137">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Standardparameter für den Druck Prozessor angibt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-138">**psecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="4c81a-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-139">Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="4c81a-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="4c81a-140">Dieser Member kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4c81a-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-141">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4c81a-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-142">Die Drucker Attribute.</span><span class="sxs-lookup"><span data-stu-id="4c81a-142">The printer attributes.</span></span> <span data-ttu-id="4c81a-143">Dieser Member kann eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="4c81a-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="4c81a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="4c81a-144">Value</span></span>                                   | <span data-ttu-id="4c81a-145">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4c81a-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c81a-146">Drucker \_ Attribut \_ Direct</span><span class="sxs-lookup"><span data-stu-id="4c81a-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="4c81a-147">Der Auftrag wird direkt an den Drucker gesendet (er ist nicht Spoolvorgang).</span><span class="sxs-lookup"><span data-stu-id="4c81a-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="4c81a-148">das Drucker \_ Attribut ist \_ \_ \_ zuerst fertig.</span><span class="sxs-lookup"><span data-stu-id="4c81a-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="4c81a-149">Wenn Set und Printer für Druck-während-Spoolvorgänge festgelegt sind, werden alle Aufträge, für die das Spoolvorgang abgeschlossen wurde, vor Aufträgen gedruckt, für die das Spoolvorgang noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4c81a-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="4c81a-150">Drucker \_ Attribut \_ Aktivieren von \_ devq</span><span class="sxs-lookup"><span data-stu-id="4c81a-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="4c81a-151">Wenn festgelegt, wird **devqueryprint** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4c81a-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="4c81a-152">**Devqueryprint** schlägt möglicherweise fehl, wenn die Dokument-und Drucker Einrichtung nicht identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4c81a-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="4c81a-153">Das Festlegen dieses Flags bewirkt, dass nicht übereinstimmende Dokumente in der Warteschlange gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="4c81a-154">Drucker \_ Attribut \_ ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="4c81a-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="4c81a-155">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="4c81a-156">Drucker \_ Attribut \_ KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="4c81a-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="4c81a-157">Wenn festgelegt, werden die Aufträge nach dem Drucken beibehalten.</span><span class="sxs-lookup"><span data-stu-id="4c81a-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="4c81a-158">Wenn der Wert nicht festgelegt ist, werden Aufträge gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4c81a-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="4c81a-159">Drucker \_ Attribut \_ lokal</span><span class="sxs-lookup"><span data-stu-id="4c81a-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="4c81a-160">Der Drucker ist ein lokaler Drucker.</span><span class="sxs-lookup"><span data-stu-id="4c81a-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="4c81a-161">Drucker \_ Attribut \_ Netzwerk</span><span class="sxs-lookup"><span data-stu-id="4c81a-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="4c81a-162">Der Drucker ist eine Netzwerkdrucker Verbindung.</span><span class="sxs-lookup"><span data-stu-id="4c81a-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="4c81a-163">Drucker \_ Attribut \_ veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="4c81a-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="4c81a-164">Gibt an, ob der Drucker im Verzeichnisdienst veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="4c81a-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="4c81a-165">Drucker \_ Attribut in \_ Warteschlange eingereiht</span><span class="sxs-lookup"><span data-stu-id="4c81a-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="4c81a-166">Wenn diese Einstellung festgelegt ist, wird der Drucker vor dem Spoolvorgang gedruckt und der Druckvorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="4c81a-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="4c81a-167">Wenn nicht festgelegt und Drucker \_ Attribut \_ Direct nicht festgelegt ist, wird der Drucker beim Spoolvorgang Spool und druckt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="4c81a-168">Drucker \_ Attribut \_ \_ nur RAW</span><span class="sxs-lookup"><span data-stu-id="4c81a-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="4c81a-169">Gibt an, dass nur unformatierte Datentypen Druckaufträge gespoolte werden können.</span><span class="sxs-lookup"><span data-stu-id="4c81a-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="4c81a-170">Drucker \_ Attribut frei \_ gegeben</span><span class="sxs-lookup"><span data-stu-id="4c81a-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="4c81a-171">Der Drucker ist freigegeben.</span><span class="sxs-lookup"><span data-stu-id="4c81a-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="4c81a-172">In Windows XP und höheren Versionen von Windows kann auch der folgende Wert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="4c81a-173">Wert</span><span class="sxs-lookup"><span data-stu-id="4c81a-173">Value</span></span>                   | <span data-ttu-id="4c81a-174">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4c81a-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c81a-175">Drucker \_ Attribut \_ Fax</span><span class="sxs-lookup"><span data-stu-id="4c81a-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="4c81a-176">Wenn festgelegt, ist der Drucker ein Faxdrucker.</span><span class="sxs-lookup"><span data-stu-id="4c81a-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="4c81a-177">Dies kann nur von [**addprinter**](addprinter.md)festgelegt werden, kann jedoch von [**enumprinter**](enumprinters.md) und [**GetPrinter**](getprinter.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="4c81a-178">In Windows Vista und höheren Versionen von Windows können auch die folgenden Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="4c81a-179">Wert</span><span class="sxs-lookup"><span data-stu-id="4c81a-179">Value</span></span>                               | <span data-ttu-id="4c81a-180">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4c81a-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4c81a-181">Anzeige \_ Name des Drucker Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c81a-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="4c81a-182">Ein Computer hat eine Verbindung mit diesem Drucker hergestellt und einen anzeigen Amen erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c81a-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="4c81a-183">Drucker \_ Attribut \_ Computer</span><span class="sxs-lookup"><span data-stu-id="4c81a-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="4c81a-184">Der Drucker ist eine Computer spezifische Verbindung.</span><span class="sxs-lookup"><span data-stu-id="4c81a-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="4c81a-185">Drucker \_ Attribut mit \_ pushübertragung für \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="4c81a-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="4c81a-186">Der Drucker wurde mithilfe der Benutzer Richtlinie "Push Printer Connections" installiert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="4c81a-187">Drucker \_ Attribut \_ mit \_ gedrückter Maschine</span><span class="sxs-lookup"><span data-stu-id="4c81a-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="4c81a-188">Der Drucker wurde mithilfe der Computer Richtlinie "Push Printer Connections" installiert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="4c81a-189">In Windows Server 2003 kann auch der folgende Wert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="4c81a-190">Wert</span><span class="sxs-lookup"><span data-stu-id="4c81a-190">Value</span></span>                  | <span data-ttu-id="4c81a-191">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4c81a-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4c81a-192">Drucker \_ Attribut \_ TS</span><span class="sxs-lookup"><span data-stu-id="4c81a-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="4c81a-193">Gibt an, dass der Drucker zurzeit über einen Terminal Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4c81a-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="4c81a-194">**Priority**</span><span class="sxs-lookup"><span data-stu-id="4c81a-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-195">Ein Prioritätswert, den der Spooler zum Weiterleiten von Druckaufträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c81a-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-196">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="4c81a-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-197">Der Standard Prioritätswert, der jedem Druckauftrag zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4c81a-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4c81a-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-199">Die früheste Uhrzeit, zu der der Drucker einen Auftrag druckt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="4c81a-200">Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="4c81a-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-201">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4c81a-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-202">Der letzte Zeitpunkt, zu dem der Drucker einen Auftrag druckt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="4c81a-203">Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr GMT (Greenwich Mean Time) verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="4c81a-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-204">**Status**</span><span class="sxs-lookup"><span data-stu-id="4c81a-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-205">Der Druckerstatus.</span><span class="sxs-lookup"><span data-stu-id="4c81a-205">The printer status.</span></span> <span data-ttu-id="4c81a-206">Dieser Member kann eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="4c81a-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="4c81a-207">Wert</span><span class="sxs-lookup"><span data-stu-id="4c81a-207">Value</span></span>                               | <span data-ttu-id="4c81a-208">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4c81a-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4c81a-209">Drucker \_ Status \_ ausgelastet</span><span class="sxs-lookup"><span data-stu-id="4c81a-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="4c81a-210">Der Drucker ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="4c81a-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="4c81a-211">\_ \_ druckerstatustür \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="4c81a-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="4c81a-212">Die Drucker Tür ist offen.</span><span class="sxs-lookup"><span data-stu-id="4c81a-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="4c81a-213">Drucker \_ Status \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="4c81a-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="4c81a-214">Der Drucker weist einen Fehlerzustand auf.</span><span class="sxs-lookup"><span data-stu-id="4c81a-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="4c81a-215">Drucker \_ Status wird \_ initialisiert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="4c81a-216">Der Drucker wird zurzeit initialisiert.</span><span class="sxs-lookup"><span data-stu-id="4c81a-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="4c81a-217">Drucker Status-e/a \_ \_ \_ aktiv</span><span class="sxs-lookup"><span data-stu-id="4c81a-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="4c81a-218">Der Drucker befindet sich in einem aktiven Eingabe-/ausgabezustand.</span><span class="sxs-lookup"><span data-stu-id="4c81a-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="4c81a-219">\_manueller Drucker Status- \_ \_ Feed</span><span class="sxs-lookup"><span data-stu-id="4c81a-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="4c81a-220">Der Drucker befindet sich in einem manuellen Feed-Zustand.</span><span class="sxs-lookup"><span data-stu-id="4c81a-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="4c81a-221">Drucker \_ Status \_ nicht \_ Toner</span><span class="sxs-lookup"><span data-stu-id="4c81a-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="4c81a-222">Im Drucker ist kein Toner vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="4c81a-223">Drucker \_ Status \_ nicht \_ verfügbar</span><span class="sxs-lookup"><span data-stu-id="4c81a-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="4c81a-224">Der Drucker ist nicht zum Drucken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4c81a-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="4c81a-225">Drucker \_ Status \_ Offline</span><span class="sxs-lookup"><span data-stu-id="4c81a-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="4c81a-226">Der Drucker ist offline.</span><span class="sxs-lookup"><span data-stu-id="4c81a-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="4c81a-227">Drucker \_ Status \_ nicht genügend Arbeits \_ \_ Speicher</span><span class="sxs-lookup"><span data-stu-id="4c81a-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="4c81a-228">Der Drucker verfügt nicht über genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4c81a-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="4c81a-229">Drucker \_ Status- \_ Ausgabe \_ bin \_ voll</span><span class="sxs-lookup"><span data-stu-id="4c81a-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="4c81a-230">Das Ausgabefach des Druckers ist voll.</span><span class="sxs-lookup"><span data-stu-id="4c81a-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="4c81a-231">Drucker \_ Status \_ Seite \_ Punt</span><span class="sxs-lookup"><span data-stu-id="4c81a-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="4c81a-232">Der Drucker kann die aktuelle Seite nicht drucken.</span><span class="sxs-lookup"><span data-stu-id="4c81a-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="4c81a-233">Drucker \_ Status \_ Papier \_ Stau</span><span class="sxs-lookup"><span data-stu-id="4c81a-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="4c81a-234">Das Papier ist im Drucker gejammt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="4c81a-235">Drucker \_ Status \_ Papier \_ out</span><span class="sxs-lookup"><span data-stu-id="4c81a-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="4c81a-236">Der Drucker ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="4c81a-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="4c81a-237">Problem mit dem Drucker \_ Status \_ Papier \_</span><span class="sxs-lookup"><span data-stu-id="4c81a-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="4c81a-238">Der Drucker hat ein Papier Problem.</span><span class="sxs-lookup"><span data-stu-id="4c81a-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="4c81a-239">Drucker \_ Status \_ angehalten</span><span class="sxs-lookup"><span data-stu-id="4c81a-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="4c81a-240">Der Drucker ist angehalten.</span><span class="sxs-lookup"><span data-stu-id="4c81a-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="4c81a-241">Drucker \_ Status \_ Ausstehend \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="4c81a-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="4c81a-242">Der Drucker wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4c81a-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="4c81a-243">Drucker \_ Status- \_ Energie \_ Spar Speicher</span><span class="sxs-lookup"><span data-stu-id="4c81a-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="4c81a-244">Der Drucker befindet sich im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="4c81a-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="4c81a-245">Drucker \_ Status \_ Drucken</span><span class="sxs-lookup"><span data-stu-id="4c81a-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="4c81a-246">Der Drucker wird gedruckt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="4c81a-247">Drucker \_ Status \_ Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="4c81a-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="4c81a-248">Der Drucker verarbeitet einen Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="4c81a-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="4c81a-249">Drucker \_ Status \_ Server \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="4c81a-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="4c81a-250">Der Druckerstatus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="4c81a-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="4c81a-251">Drucker \_ Status- \_ Toner \_ niedrig</span><span class="sxs-lookup"><span data-stu-id="4c81a-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="4c81a-252">Der Drucker ist niedrig auf dem Toner.</span><span class="sxs-lookup"><span data-stu-id="4c81a-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="4c81a-253">Drucker \_ Status \_ Benutzer \_ Eingriff</span><span class="sxs-lookup"><span data-stu-id="4c81a-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="4c81a-254">Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer eine Aktion durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="4c81a-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="4c81a-255">Drucker \_ Status \_ wartet</span><span class="sxs-lookup"><span data-stu-id="4c81a-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="4c81a-256">Der Drucker wartet.</span><span class="sxs-lookup"><span data-stu-id="4c81a-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="4c81a-257">Drucker \_ Status \_ \_ Aufwärmphase</span><span class="sxs-lookup"><span data-stu-id="4c81a-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="4c81a-258">Der Drucker befindet sich in der Aufwärmphase.</span><span class="sxs-lookup"><span data-stu-id="4c81a-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="4c81a-259">**cjobs**</span><span class="sxs-lookup"><span data-stu-id="4c81a-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-260">Die Anzahl der Druckaufträge, die für den Drucker in die Warteschlange eingereiht wurden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4c81a-261">**AveragePPM**</span><span class="sxs-lookup"><span data-stu-id="4c81a-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="4c81a-262">Die durchschnittliche Anzahl der Seiten pro Minute, die auf dem Drucker gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="4c81a-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c81a-263">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c81a-263">Requirements</span></span>



| <span data-ttu-id="4c81a-264">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c81a-264">Requirement</span></span> | <span data-ttu-id="4c81a-265">Wert</span><span class="sxs-lookup"><span data-stu-id="4c81a-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c81a-266">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c81a-266">Minimum supported client</span></span><br/> | <span data-ttu-id="4c81a-267">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c81a-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4c81a-268">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c81a-268">Minimum supported server</span></span><br/> | <span data-ttu-id="4c81a-269">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c81a-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4c81a-270">Header</span><span class="sxs-lookup"><span data-stu-id="4c81a-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c81a-271"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c81a-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4c81a-272">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="4c81a-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4c81a-273">**\_ Drucker \_ Info \_ 2W** (Unicode) und **\_ Drucker \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4c81a-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4c81a-274">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c81a-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c81a-275">Drucken</span><span class="sxs-lookup"><span data-stu-id="4c81a-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4c81a-276">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4c81a-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4c81a-277">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="4c81a-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="4c81a-278">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="4c81a-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="4c81a-279">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4c81a-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="4c81a-280">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4c81a-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="4c81a-281">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4c81a-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="4c81a-282">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4c81a-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

