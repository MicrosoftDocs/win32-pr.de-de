---
description: Die Drucker \_ Info \_ 6 gibt den Statuswert eines Druckers an.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: PRINTER_INFO_6 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360825"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="c177e-103">Drucker \_ Info \_ 6-Struktur</span><span class="sxs-lookup"><span data-stu-id="c177e-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="c177e-104">Die **Drucker \_ Info \_ 6** gibt den Statuswert eines Druckers an.</span><span class="sxs-lookup"><span data-stu-id="c177e-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c177e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c177e-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="c177e-106">Member</span><span class="sxs-lookup"><span data-stu-id="c177e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c177e-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="c177e-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c177e-108">Der Druckerstatus.</span><span class="sxs-lookup"><span data-stu-id="c177e-108">The printer status.</span></span> <span data-ttu-id="c177e-109">Dieser Member kann eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c177e-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="c177e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c177e-110">Value</span></span>                               | <span data-ttu-id="c177e-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c177e-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c177e-112">Drucker \_ Status \_ ausgelastet</span><span class="sxs-lookup"><span data-stu-id="c177e-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="c177e-113">Der Drucker ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="c177e-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="c177e-114">\_ \_ druckerstatustür \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="c177e-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="c177e-115">Die Drucker Tür ist offen.</span><span class="sxs-lookup"><span data-stu-id="c177e-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="c177e-116">Drucker \_ Status \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="c177e-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="c177e-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c177e-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="c177e-118">Drucker \_ Status wird \_ initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c177e-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="c177e-119">Der Drucker wird zurzeit initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c177e-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="c177e-120">Drucker Status-e/a \_ \_ \_ aktiv</span><span class="sxs-lookup"><span data-stu-id="c177e-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="c177e-121">Der Drucker befindet sich in einem aktiven Eingabe-/ausgabezustand.</span><span class="sxs-lookup"><span data-stu-id="c177e-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="c177e-122">\_manueller Drucker Status- \_ \_ Feed</span><span class="sxs-lookup"><span data-stu-id="c177e-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="c177e-123">Der Drucker befindet sich in einem manuellen Feed-Zustand.</span><span class="sxs-lookup"><span data-stu-id="c177e-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="c177e-124">Drucker \_ Status \_ nicht \_ Toner</span><span class="sxs-lookup"><span data-stu-id="c177e-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="c177e-125">Im Drucker ist kein Toner vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c177e-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="c177e-126">Drucker \_ Status \_ nicht \_ verfügbar</span><span class="sxs-lookup"><span data-stu-id="c177e-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="c177e-127">Der Drucker ist nicht zum Drucken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c177e-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="c177e-128">Drucker \_ Status \_ Offline</span><span class="sxs-lookup"><span data-stu-id="c177e-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="c177e-129">Der Drucker ist offline.</span><span class="sxs-lookup"><span data-stu-id="c177e-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="c177e-130">Drucker \_ Status \_ nicht genügend Arbeits \_ \_ Speicher</span><span class="sxs-lookup"><span data-stu-id="c177e-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="c177e-131">Der Drucker verfügt nicht über genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c177e-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="c177e-132">Drucker \_ Status- \_ Ausgabe \_ bin \_ voll</span><span class="sxs-lookup"><span data-stu-id="c177e-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="c177e-133">Das Ausgabefach des Druckers ist voll.</span><span class="sxs-lookup"><span data-stu-id="c177e-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="c177e-134">Drucker \_ Status \_ Seite \_ Punt</span><span class="sxs-lookup"><span data-stu-id="c177e-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="c177e-135">Der Drucker kann die aktuelle Seite nicht drucken.</span><span class="sxs-lookup"><span data-stu-id="c177e-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="c177e-136">Drucker \_ Status \_ Papier \_ Stau</span><span class="sxs-lookup"><span data-stu-id="c177e-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="c177e-137">Das Papier ist im Drucker gejammt.</span><span class="sxs-lookup"><span data-stu-id="c177e-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="c177e-138">Drucker \_ Status \_ Papier \_ out</span><span class="sxs-lookup"><span data-stu-id="c177e-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="c177e-139">Der Drucker ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="c177e-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="c177e-140">Problem mit dem Drucker \_ Status \_ Papier \_</span><span class="sxs-lookup"><span data-stu-id="c177e-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="c177e-141">Der Drucker hat ein Papier Problem.</span><span class="sxs-lookup"><span data-stu-id="c177e-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="c177e-142">Drucker \_ Status \_ angehalten</span><span class="sxs-lookup"><span data-stu-id="c177e-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="c177e-143">Der Drucker ist angehalten.</span><span class="sxs-lookup"><span data-stu-id="c177e-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="c177e-144">Drucker \_ Status \_ Ausstehend \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="c177e-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="c177e-145">Der Drucker steht aufgrund eines Aufrufens der [**deleteprinter**](deleteprinter.md) -Funktion für das Löschen aus.</span><span class="sxs-lookup"><span data-stu-id="c177e-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="c177e-146">Drucker \_ Status- \_ Energie \_ Spar Speicher</span><span class="sxs-lookup"><span data-stu-id="c177e-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="c177e-147">Der Drucker befindet sich im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="c177e-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="c177e-148">Drucker \_ Status \_ Drucken</span><span class="sxs-lookup"><span data-stu-id="c177e-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="c177e-149">Der Drucker wird gedruckt.</span><span class="sxs-lookup"><span data-stu-id="c177e-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="c177e-150">Drucker \_ Status \_ Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="c177e-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="c177e-151">Der Drucker verarbeitet einen Befehl aus der Funktion " [**SetPrinter**](setprinter.md) ".</span><span class="sxs-lookup"><span data-stu-id="c177e-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="c177e-152">Drucker \_ Status \_ Server \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="c177e-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="c177e-153">Der Druckerstatus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c177e-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="c177e-154">Drucker \_ Status- \_ Toner \_ niedrig</span><span class="sxs-lookup"><span data-stu-id="c177e-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="c177e-155">Der Drucker ist niedrig auf dem Toner.</span><span class="sxs-lookup"><span data-stu-id="c177e-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="c177e-156">Drucker \_ Status \_ Benutzer \_ Eingriff</span><span class="sxs-lookup"><span data-stu-id="c177e-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="c177e-157">Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer eine Aktion durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="c177e-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="c177e-158">Drucker \_ Status \_ wartet</span><span class="sxs-lookup"><span data-stu-id="c177e-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="c177e-159">Der Drucker wartet.</span><span class="sxs-lookup"><span data-stu-id="c177e-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="c177e-160">Drucker \_ Status \_ \_ Aufwärmphase</span><span class="sxs-lookup"><span data-stu-id="c177e-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="c177e-161">Der Drucker befindet sich in der Aufwärmphase.</span><span class="sxs-lookup"><span data-stu-id="c177e-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c177e-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c177e-162">Requirements</span></span>



| <span data-ttu-id="c177e-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c177e-163">Requirement</span></span> | <span data-ttu-id="c177e-164">Wert</span><span class="sxs-lookup"><span data-stu-id="c177e-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c177e-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c177e-165">Minimum supported client</span></span><br/> | <span data-ttu-id="c177e-166">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c177e-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c177e-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c177e-167">Minimum supported server</span></span><br/> | <span data-ttu-id="c177e-168">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c177e-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c177e-169">Header</span><span class="sxs-lookup"><span data-stu-id="c177e-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="c177e-170"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c177e-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c177e-171">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c177e-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c177e-172">**\_ Drucker \_ Info \_ 6W** (Unicode) und **\_ Drucker \_ Info \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c177e-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c177e-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c177e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c177e-174">Drucken</span><span class="sxs-lookup"><span data-stu-id="c177e-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c177e-175">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c177e-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c177e-176">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c177e-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="c177e-177">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c177e-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c177e-178">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c177e-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="c177e-179">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c177e-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="c177e-180">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c177e-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="c177e-181">**Drucker \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="c177e-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 




