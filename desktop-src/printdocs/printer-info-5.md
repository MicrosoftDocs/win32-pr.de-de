---
description: Die Drucker \_ Info \_ 5-Struktur gibt ausführliche Drucker Informationen an.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: PRINTER_INFO_5 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352400"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="c1716-103">Drucker \_ Info \_ 5-Struktur</span><span class="sxs-lookup"><span data-stu-id="c1716-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="c1716-104">Die **Drucker \_ Info \_ 5** -Struktur gibt ausführliche Drucker Informationen an.</span><span class="sxs-lookup"><span data-stu-id="c1716-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1716-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1716-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="c1716-106">Member</span><span class="sxs-lookup"><span data-stu-id="c1716-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1716-107">**pprintername**</span><span class="sxs-lookup"><span data-stu-id="c1716-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="c1716-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt.</span><span class="sxs-lookup"><span data-stu-id="c1716-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="c1716-109">**pportname**</span><span class="sxs-lookup"><span data-stu-id="c1716-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="c1716-110">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1716-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="c1716-111">Wenn ein Drucker mit mehr als einem Port verbunden ist, müssen die Namen der einzelnen Ports durch Kommas getrennt werden (z. b. "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="c1716-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="c1716-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c1716-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="c1716-113">Die Drucker Attribute.</span><span class="sxs-lookup"><span data-stu-id="c1716-113">The printer attributes.</span></span> <span data-ttu-id="c1716-114">Dieser Member kann eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c1716-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="c1716-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c1716-115">Value</span></span>                                   | <span data-ttu-id="c1716-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1716-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1716-117">Drucker \_ Attribut \_ Direct</span><span class="sxs-lookup"><span data-stu-id="c1716-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="c1716-118">Der Auftrag wird direkt an den Drucker gesendet (er ist nicht Spoolvorgang).</span><span class="sxs-lookup"><span data-stu-id="c1716-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="c1716-119">das Drucker \_ Attribut ist \_ \_ \_ zuerst fertig.</span><span class="sxs-lookup"><span data-stu-id="c1716-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="c1716-120">Wenn Set und Printer für Druck-während-Spoolvorgänge festgelegt sind, werden alle Aufträge, für die das Spoolvorgang abgeschlossen wurde, vor Aufträgen gedruckt, für die das Spoolvorgang noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c1716-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="c1716-121">Drucker \_ Attribut \_ Aktivieren von \_ devq</span><span class="sxs-lookup"><span data-stu-id="c1716-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="c1716-122">Wenn festgelegt, wird **devqueryprint** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c1716-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="c1716-123">**Devqueryprint** schlägt möglicherweise fehl, wenn die Dokument-und Drucker Einrichtung nicht identisch ist.</span><span class="sxs-lookup"><span data-stu-id="c1716-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="c1716-124">Das Festlegen dieses Flags bewirkt, dass nicht übereinstimmende Dokumente in der Warteschlange gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c1716-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="c1716-125">Drucker \_ Attribut \_ ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="c1716-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="c1716-126">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c1716-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c1716-127">Drucker \_ Attribut \_ KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="c1716-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="c1716-128">Wenn festgelegt, werden die Aufträge nach dem Drucken beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c1716-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="c1716-129">Wenn der Wert nicht festgelegt ist, werden Aufträge gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c1716-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="c1716-130">Drucker \_ Attribut \_ lokal</span><span class="sxs-lookup"><span data-stu-id="c1716-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="c1716-131">Der Drucker ist ein lokaler Drucker.</span><span class="sxs-lookup"><span data-stu-id="c1716-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="c1716-132">Drucker \_ Attribut \_ Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c1716-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="c1716-133">Der Drucker ist eine Netzwerkdrucker Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c1716-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="c1716-134">Drucker \_ Attribut \_ veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="c1716-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="c1716-135">Gibt an, ob der Drucker im Verzeichnisdienst veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="c1716-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="c1716-136">Drucker \_ Attribut in \_ Warteschlange eingereiht</span><span class="sxs-lookup"><span data-stu-id="c1716-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="c1716-137">Wenn diese Einstellung festgelegt ist, wird der Drucker vor dem Spoolvorgang gedruckt und der Druckvorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="c1716-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="c1716-138">Wenn nicht festgelegt und Drucker \_ Attribut \_ Direct nicht festgelegt ist, wird der Drucker beim Spoolvorgang Spool und druckt.</span><span class="sxs-lookup"><span data-stu-id="c1716-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="c1716-139">Drucker \_ Attribut \_ \_ nur RAW</span><span class="sxs-lookup"><span data-stu-id="c1716-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="c1716-140">Gibt an, dass nur unformatierte Datentypen Druckaufträge gespoolte werden können.</span><span class="sxs-lookup"><span data-stu-id="c1716-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="c1716-141">Drucker \_ Attribut frei \_ gegeben</span><span class="sxs-lookup"><span data-stu-id="c1716-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="c1716-142">Der Drucker ist freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c1716-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="c1716-143">In Windows XP und höheren Versionen von Windows kann auch der folgende Wert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1716-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="c1716-144">Wert</span><span class="sxs-lookup"><span data-stu-id="c1716-144">Value</span></span>                   | <span data-ttu-id="c1716-145">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1716-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1716-146">Drucker \_ Attribut \_ Fax</span><span class="sxs-lookup"><span data-stu-id="c1716-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="c1716-147">Wenn festgelegt, ist der Drucker ein Faxdrucker.</span><span class="sxs-lookup"><span data-stu-id="c1716-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="c1716-148">Dies kann nur von [**addprinter**](addprinter.md)festgelegt werden, kann jedoch von [**enumprinter**](enumprinters.md) und [**GetPrinter**](getprinter.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c1716-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="c1716-149">In Windows Vista und höheren Versionen von Windows können auch die folgenden Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1716-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="c1716-150">Wert</span><span class="sxs-lookup"><span data-stu-id="c1716-150">Value</span></span>                               | <span data-ttu-id="c1716-151">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1716-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c1716-152">Anzeige \_ Name des Drucker Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="c1716-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="c1716-153">Ein Computer hat eine Verbindung mit diesem Drucker hergestellt und einen anzeigen Amen erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1716-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="c1716-154">Drucker \_ Attribut \_ Computer</span><span class="sxs-lookup"><span data-stu-id="c1716-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="c1716-155">Der Drucker ist eine Computer spezifische Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c1716-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="c1716-156">Drucker \_ Attribut mit \_ pushübertragung für \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="c1716-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="c1716-157">Der Drucker wurde mithilfe der Benutzer Richtlinie "Push Printer Connections" installiert.</span><span class="sxs-lookup"><span data-stu-id="c1716-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="c1716-158">Drucker \_ Attribut \_ mit \_ gedrückter Maschine</span><span class="sxs-lookup"><span data-stu-id="c1716-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="c1716-159">Der Drucker wurde mithilfe der Computer Richtlinie "Push Printer Connections" installiert.</span><span class="sxs-lookup"><span data-stu-id="c1716-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c1716-160">**Devicenotselectedtimeout**</span><span class="sxs-lookup"><span data-stu-id="c1716-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c1716-161">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1716-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1716-162">**Transmissionretrytimeout**</span><span class="sxs-lookup"><span data-stu-id="c1716-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c1716-163">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1716-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1716-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1716-164">Requirements</span></span>



| <span data-ttu-id="c1716-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1716-165">Requirement</span></span> | <span data-ttu-id="c1716-166">Wert</span><span class="sxs-lookup"><span data-stu-id="c1716-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1716-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1716-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c1716-168">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1716-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1716-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1716-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c1716-170">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1716-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c1716-171">Header</span><span class="sxs-lookup"><span data-stu-id="c1716-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1716-172"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1716-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c1716-173">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c1716-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c1716-174">**\_ Drucker \_ Info \_ 5W** (Unicode) und **\_ Drucker \_ Info \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c1716-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c1716-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1716-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1716-176">Drucken</span><span class="sxs-lookup"><span data-stu-id="c1716-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c1716-177">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c1716-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c1716-178">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="c1716-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="c1716-179">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c1716-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="c1716-180">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c1716-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="c1716-181">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c1716-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c1716-182">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c1716-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="c1716-183">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c1716-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="c1716-184">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c1716-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




